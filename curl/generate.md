# DeepSeek V4 cURL Examples

Use this request to call deepseek-v4-flash with the OpenAI-style chat completions endpoint.

```bash
export POYO_API_KEY="YOUR_POYO_API_KEY_HERE"
export POYO_BASE_URL="https://api.poyo.ai"

curl --fail-with-body --request POST \
  --url "$POYO_BASE_URL/v1/chat/completions" \
  --header "Authorization: Bearer $POYO_API_KEY" \
  --header "Content-Type: application/json" \
  --data '{
  "model": "deepseek-v4-flash",
  "messages": [
    {
      "role": "system",
      "content": "You are a concise senior engineering assistant."
    },
    {
      "role": "user",
      "content": "Review this API integration plan and list the most likely production risks."
    }
  ],
  "max_tokens": 600
}'
```

To switch model variants, change `model`. For example:

```json
{ "model": "deepseek-v4-pro" }
```

## Expected Response Shape

```json
{
  "id": "chatcmpl-example",
  "object": "chat.completion",
  "model": "deepseek-v4-flash",
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "..."
      },
      "finish_reason": "stop"
    }
  ],
  "usage": {
    "prompt_tokens": 123,
    "completion_tokens": 456,
    "total_tokens": 579
  }
}
```
