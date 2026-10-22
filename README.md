# Book Store Frontend

A single static page (`index.html`, plain HTML, CSS and JavaScript) that talks to the
`book_store_api` repo. It exists to show how a separate frontend uses a JSON API.

## What it does

- Lists books with search, a bestsellers filter and Previous / Next pagination
- Logs in with a token (stored in the browser) and adds books through the API
- Shows the API's validation errors and handles an expired login

## Run it

1. Start the API from `book_store_api` on port 8001 (`python manage.py runserver 8001`).
2. Serve this folder on port 8002:

```bash
python -m http.server 8002 --bind 127.0.0.1
```

3. Open http://127.0.0.1:8002/

The API address is the `API` constant at the top of the script in `index.html`.
Port 8002 must be listed in the API's `CORS_ALLOWED_ORIGINS`, or the browser will block the calls.
