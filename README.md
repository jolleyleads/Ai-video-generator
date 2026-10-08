# AI Video Studio

Mobile-friendly text-to-video web application hosted on Render. Backend proxies requests to Replicate, keeping the API token off the browser.

## Setup
- Node.js 20+
- Set `REPLICATE_API_TOKEN` in Render's environment settings.
- Optionally set `REPLICATE_MODEL` to a supported public Replicate video model (default `minimax/video-01`). Confirm model input schema and access with the provider.
- Build command: `npm install`
- Start command: `npm start`

## Limitations
- Text-to-video only in V1. Voiceover, image-to-video, music, project storage, authentication, and video stitching are not implemented.
- Aspect ratio and style are appended to the prompt; model support varies.
- Provider charges apply. Avoid exposing this unauthenticated app publicly with a paid API key until rate limiting/authentication are added.
- Jobs are held in memory and lost when the service restarts.
