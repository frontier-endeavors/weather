# Manhattan Weather

Personal Manhattan, KS weather + Wildcat Creek dashboard.

## Local preview

Live data needs `http://` (not opening the file directly):

```bash
cd ~/code/weather
python3 -m http.server 8080
open http://127.0.0.1:8080
```

## Deploy (Cloudflare Pages)

Upload this folder / connect the git repo in Workers & Pages → Create → Pages.

Optional custom domain: `weather.memoryspace.cc`

## Data sources

- Snapshot embedded for instant first paint
- Live: NWS hourly, MET Norway 10-day, USGS creek, RainViewer radar
