

## V1.6 troubleshooting

- GitHub Pages cannot run this Node.js backend; deploy this folder on a Node.js host with HTTPS.
- Set `ALLOWED_ORIGIN=https://opywp.github.io` (no trailing slash).
- Set `WORKSHOP_TOKEN` to a long random access token and enter the same token in Workshop Settings.
- Set `AI_API_KEY`, `AI_MODEL`, and `AI_CHAT_URL` for your provider. `AI_CHAT_URL` must be an HTTPS OpenAI-compatible chat completions endpoint.
- Set the host's start command to `node server.mjs` and make sure it supplies `PORT`.
- Test the `/health` endpoint from Workshop Settings; then send a message. `/health` only checks backend authorization, not provider credentials.
- If provider requests fail, inspect hosting logs; never paste secrets into public GitHub code.
- Keep access tokens private. Browser users can see tokens they enter; this is a personal development setup, not multi-user authentication.
