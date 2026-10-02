# Jev API quickstart

Endpoint: `POST https://api.typesafe.ai/v1/systemone`. Header: `Authorization: Bearer $TYPESAFE_API_KEY`.

```bash
curl https://api.typesafe.ai/v1/systemone \
  -H "Authorization: Bearer $TYPESAFE_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "jev-latest",
    "state": {"post": "Breaking: we just shipped v2, live today."},
    "questions": {
      "type": {"type": "choice",
               "instructions": "Which category is `post`?",
               "criteria": {"news": "A launch or announcement", "opinion": "A personal take", "spam": "Bait with no content"}},
      "is_bait": {"type": "noul",
                  "instructions": "Is `post` engagement bait?",
                  "criteria": {"true": "bait", "false": "genuine"}},
      "quality": {"type": "score",
                  "instructions": "How specific and useful is `post`?",
                  "criteria": ["Generic filler", "Vague", "One real idea", "Specific and useful", "Exceptional"]}
    }
  }'
```

## What comes back

An `answers` object with one entry per question. Noul gives a probability from 0 to 1. Choice gives the winning option, a probability for each option and a confidence. Score gives a value that can fall between levels, with a legend, probabilities and a confidence. Output tokens are free and no text is generated.

## Rules

- Put many questions in one request. That is the cheap way to use it.
- `jev-latest` currently points to `jev-1.13.0`. Pin `jev-1.13.0` to keep it stable.
- Limits: 1,200 requests per minute and 250,000 tokens per second. Context is 32k tokens for state plus the longest question, and 64k per request.
- Errors: 401 bad key, 422 malformed question, 429 rate limit, 529 overload.

Source for prices and limits: TypeSafe's documentation and model pages, as read on 2026-09-19. Check them before you build.
