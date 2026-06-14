# Bagisto GraphQL API

## Description

Bagisto provides a GraphQL API built on the [Lighthouse](https://lighthouse-php.com/) PHP GraphQL server library. The API covers both a **Shop API** (storefront, public and authenticated customer operations) and an **Admin API** (full back-office management). It is delivered by the [bagisto/headless-ecommerce](https://github.com/bagisto/headless-ecommerce) package.

## Endpoint

```
POST https://{your-domain}/graphql
```

All GraphQL operations are sent as HTTP POST requests to a single endpoint. The endpoint accepts `application/json` bodies with a `query` string and optional `variables` object.

## Authentication

| Guard | Token Type | Header |
|---|---|---|
| Shop API (`api`) | Laravel Sanctum (Bearer) | `Authorization: Bearer {token}` |
| Admin API (`admin-api`) | Laravel Sanctum (Bearer) | `Authorization: Bearer {token}` |

Obtain a shop token via the `customerLogin` mutation. Admin tokens are issued from the admin panel or the admin authentication endpoint.

## Coverage

The schema is organized into two namespaces that share many types:

### Shop (Storefront)

- **Session** — `customerLogin`, `customerLogout`
- **Account** — `accountInfo`, `updateAccount`, `deleteAccount`
- **Registration** — `customerRegister`, resend verification
- **Addresses** — `customerAddresses`, `createCustomerAddress`, `updateCustomerAddress`, `deleteCustomerAddress`
- **Cart** — `cartDetail`, `cartItems`, `addItemToCart`, `updateItemToCart`, `removeCartItem`, `removeAllCartItem`, `moveToWishlist`
- **Checkout** — save addresses, save shipping method, save payment method, place order
- **Coupon** — `applyCoupon`, `removeCoupon`
- **Wishlist** — `wishlists`, `addToWishlist`, `removeFromWishlist`, `moveToCart`
- **Orders** — `ordersList`, `orderDetail`, `cancelCustomerOrder`, `reorder`
- **Invoices / Shipments / Refunds** — view-only via `viewInvoices`, `viewShipments`, `viewRefunds`
- **Reviews** — `customerReviews`, `createReview`, `deleteReview`
- **Compare Products** — `compareProducts`, `addToCompare`, `removeFromCompare`
- **Homepage / Catalog Browse** — `getDefaultChannel`, `homeCategories`, `allProducts`, `getFilterAttribute`, `themeCustomization`
- **Newsletter** — `subscribeToNewsletter`
- **Contact Us** — `contactUs`
- **GDPR** — customer data request

### Admin

- **Catalog — Products** — full CRUD (`products`, `product`, `createProduct`, `updateProduct`, `deleteProduct`); supports simple, configurable, grouped, bundled, downloadable, virtual, and booking product types
- **Catalog — Categories** — full CRUD
- **Catalog — Attributes** — full CRUD including attribute options and translations
- **Catalog — Attribute Families** — full CRUD
- **Customers** — full CRUD plus notes and order creation
- **Customer Groups** — full CRUD
- **Reviews** — list, approve/disapprove, delete
- **Orders** — list, detail, cancel, reorder; sub-resources: invoices, shipments, refunds, transactions
- **Invoices** — create, list, detail
- **Shipments** — create, list, detail
- **Refunds** — create, list, detail
- **CMS Pages** — full CRUD
- **Marketing — Cart Rules / Catalog Rules** — full CRUD
- **Marketing — Communications** — email templates, campaigns, events, newsletter subscribers
- **Marketing — SEO** — sitemaps, URL rewrites, search terms, search synonyms
- **Settings — Channels** — full CRUD
- **Settings — Locales / Currencies / Exchange Rates** — full CRUD
- **Settings — Inventory Sources** — full CRUD
- **Settings — Tax Rates / Tax Categories** — full CRUD
- **Settings — Roles / Users** — full CRUD
- **Settings — Themes / Push Notifications** — manage
- **Configuration** — read/write store configuration

## Schema Source

- GitHub: [bagisto/headless-ecommerce](https://github.com/bagisto/headless-ecommerce/tree/main/src/graphql)
- Entry point: `src/graphql/schema.graphql` (imports all sub-schemas via `#import`)
- Docs: https://devdocs.bagisto.com/2.x/graphql-storefront-api/

## Key Scalars

| Scalar | Description |
|---|---|
| `Date` | `Y-m-d` formatted date string |
| `DateTime` | `Y-m-d H:i:s` formatted datetime string |
| `Upload` | Multipart file upload |
| `JSON` | Arbitrary JSON value |
