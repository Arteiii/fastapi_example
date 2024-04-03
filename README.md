# FastAPI Example App

This is an example FastAPI application demonstrating basic usage with middleware and Pydantic models.

## Overview

Use default middleware to calculate request processing time and add a custom header.
Create endpoints with different HTTP methods (GET, POST, PUT).
Accept custom inputs using Pydantic models.

## Installation

### Clone the repository

Install the required dependencies:

```bash
poetry install
```

## Usage

### Run the FastAPI app

```bash
poetry run uvicorn fastapi-example.main:app --host 0.0.0.0 --port 8080
```

Open your web browser and go to <http://localhost:80> to access the app.

## Endpoints

- **GET** ``/``: A simple endpoint demonstrating a function that takes 4 seconds to respond
- **POST** ``/items/``: Create a new item with custom inputs using a Pydantic model
- **PUT** ``/items/{item_id}``: Update an existing item with custom inputs using a Pydantic mode

## Example

### Create a New Item

Send a POST request to ``/items/`` with the following JSON payload:

```json
{
  "name": "Example Item",
  "description": "This is an example item",
  "price": 10.99,
  "tax": 1.50
}
````

### Update an Existing Item

Send a PUT request to ``/items/{item_id}`` (replace ``{item_id}`` with the item's ID) with a JSON payload similar to the one used for creating an item.

## Note

This FastAPI app is an example application created for demonstration purposes.

Feel free to explore, modify, or use it as a reference for your own projects.

## License

Licensed Under the **MIT** license.

Read More in the [**LICENSE**](LICENSE.md) file.
