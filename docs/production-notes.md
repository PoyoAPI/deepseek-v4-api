# Production Notes

- Use Flash for routine backend assistant work and Pro for harder reasoning.
- Track prompt, completion, and total tokens so cost stays visible.
- Keep model switching explicit in code rather than hidden in user prompts.
- Set request timeouts and retries around network errors.
- Track token usage and latency for every model variant.
- Keep model selection explicit in server-side code.
- Keep `POYO_API_KEY` on the server.
- Do not log full prompts if they may contain user-private data.

## Security Checklist

- Never expose `POYO_API_KEY` in browser code, mobile apps, screenshots, or public logs.
- Use environment variables or a secret manager for API keys.
- Use allowlisted webhook endpoints when callbacks are enabled.
- Store request metadata separately from sensitive user content when possible.
