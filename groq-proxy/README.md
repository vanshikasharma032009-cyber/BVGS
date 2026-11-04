# Groq Proxy for the School Chatbot

The static website calls this Cloudflare Worker. The worker keeps the Groq API key
server-side and answers using text extracted from the school's public website pages.

## Deploy

1. Install Wrangler and sign in to Cloudflare:

   ```bash
   npx wrangler login
   ```

2. Set the API key as a Cloudflare secret. Wrangler prompts for the value:

   ```bash
   npx wrangler secret put GROQ_API_KEY
   ```

   Never paste the API key into website JavaScript, HTML, or this repository.

3. Deploy the worker:

   ```bash
   npx wrangler deploy
   ```

4. Copy the deployed Worker URL and set `GROQ_PROXY_URL` near the top of
   `js/chatbot.js` to that URL.

5. Serve the website over HTTP (for example, on port 8000). The chatbot fetches
   the public site pages from the same origin to provide relevant answers.
