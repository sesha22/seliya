# seliya

# Amazing Safari

[Amazing Safari](http://seliya.co.id) online store for sambal products .

## Links

- Frontend Web: <https://seliya.co.id>
- Backend API: <https://seliya-api.co.id>

Repositories:

- General: <https://github.com/sesha22/seliya>
- Backend API: <https://github.com/sesha22/seliya-api>
- Frontend Web: <https://github.com/sesha22/seliya-web>

Inspirations:

- <https://chileeoil.com>
- <https://brooklyndelhi.com/>

## Architecture & Tech Stack

### Client = Presentation Layer (UI)

- HTML
- CSS
  - Tailwind CSS
  - shadcn/ui
- JavaScript
- TypeScript
- React
- React Router
- Docker

### Server = Application Layer (Business Logic)

- JavaScript
- TypeScript
- Hono
- OpenAPI
- Zod
- Docker

### Data Access Layer (Database)

- Prisma
- PostgreSQL
- Docker

## Features

- Home page
  - Hero section
  - Products catalogue
  - Example: <https://chileeoil.com/collections/all>
- Product page
  - Image
  - SKU (stock keeping unit)
  - Name
  - Price
  - Description
  - Add to cart form: quantity input & add to cart button
- Shopping cart page
  - Product items to buy
    - Image, name, price, quantity, total (price x quantity)
    - Remove item
  - Link: continue shopping, go to products catalogue
  - Link: checkout
- Checkout page
  - Order summary
    - Product items to buy
    - Grand total of all product items to buy
- Place order / transaction is being processed

## UI Designs

- Figma: <>

### Home Page

<img alt="Home Page" src="./designs/home.jpg" width="400" />

## Entity Relationship Diagram (ERD)

![ERD](./diagrams/erd.svg)

## REST API Endpoints

- Production: ``
- Local: `http://localhost:3000`

| Endpoint         | HTTP     | Description               |
| ---------------- | -------- | ------------------------- |
| `/products`      | `GET`    | Get all products          |
| `/products/:id`  | `GET`    | Get product by id         |
| `/products/seed` | `POST`   | Seed all initial products |
| `/products`      | `POST`   | Add new product           |
| `/products`      | `DELETE` | Delete all products       |
| `/products/:id`  | `DELETE` | Delete product by id      |
| `/products/:id`  | `PUT`    | Update product by id      |

### Product

```json
{
  "id": "abc123",
  "slug": "",
  "name": "",
  "price":
}
```

### Add New Product

Request Body:

```json
{
  "name": "",
  "price": ,
  "color": ""
}
```

Response Body:

```json
{
  "id": "",
  "slug": "",
  "name": "",
  "price": ,
  "colors": ""
}
```
