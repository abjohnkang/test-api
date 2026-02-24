# test-api

A simple FastAPI-based API exposing several endpoints.

## Endpoints

- `GET /` — Returns a welcome message.
- `GET /health` — Health check endpoint; returns status.
- `GET /items/{item_id}` — Returns info about an item. Optional query param: `q`.

## Running the API

```bash
uvicorn main:app --reload
```

## Requirements

- fastapi
- uvicorn

Install dependencies:

```bash
pip install fastapi uvicorn
```

## Example Request

```bash
curl "http://localhost:8000/items/5?q=test"
```

## Response

```json
{"item_id":5,"q":"test"}
```

