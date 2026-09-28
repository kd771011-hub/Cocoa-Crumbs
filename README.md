# Cocoa & Crumbs

**Cocoa & Crumbs** is a responsive chocolate and cake shop e-commerce demo with a customer storefront and an admin dashboard.

The current project is implemented as a **single self-contained HTML file** using HTML, CSS, and vanilla JavaScript. It includes generated demo product data, shopping-cart functionality, wishlist support, checkout flow, and admin views.

---

## ✨ Features

### Customer Storefront

- Premium chocolate and bakery-themed UI
- Responsive desktop, tablet, and mobile layout
- Sticky header navigation
- Mobile bottom navigation
- Hero section
- Featured chocolates
- Best-selling cakes
- New arrivals
- Special offers
- Combo offers
- Birthday cake section
- Customer reviews
- Newsletter subscription UI
- Footer with shop/contact information

### Product Catalog

The demo generates **200 products**:

- 100 chocolate products
- 100 cake products

Product data includes:

- Product ID
- Product name
- Product type
- Category
- Description
- Price
- Original price
- Discount
- Product image
- Gallery
- Rating
- Review count
- Stock
- Weight
- Ingredients
- Featured status
- Bestseller status
- Creation date

### Shopping

- Product details page
- Product image gallery
- Wishlist
- Add to cart
- Quantity controls
- Remove from cart
- Cart summary
- Delivery calculation
- GST calculation
- Standard delivery
- Express delivery
- Checkout flow
- Order confirmation

### Cake Customization

Cake products support:

- Cake weight selection
- Message on cake
- Custom photo filename selection
- Delivery date
- Special instructions

### Search & Filters

The shop supports:

- Product search
- Category filtering
- Maximum price filtering
- Rating filtering
- Discount filtering
- In-stock filtering
- Popular sorting
- Newest sorting
- Price low-to-high
- Price high-to-low
- Highest-rated sorting
- Reset filters

### Admin Dashboard

The demo admin area includes:

- Dashboard overview
- Product management
- Add product
- Edit product
- Delete product
- Product search
- Order management
- Customer summary
- Sales analytics
- Revenue charts
- Order status updates

---

## 🛍️ Main Routes

The application uses hash-based routing.

| Route | Purpose |
|---|---|
| `#/` | Home page |
| `#/shop/chocolate` | Chocolate catalog |
| `#/shop/cake` | Cake catalog |
| `#/shop/offers` | Discounted products |
| `#/shop/best` | Best sellers |
| `#/shop/new` | New arrivals |
| `#/shop/all` | All products |
| `#/p/PRODUCT_ID` | Product details |
| `#/cart` | Shopping cart |
| `#/checkout` | Checkout |
| `#/wish` | Wishlist |
| `#/about` | About/contact information |
| `#/admin` | Admin dashboard |
| `#/admin/dash` | Dashboard overview |
| `#/admin/prod` | Product management |
| `#/admin/ord` | Order management |
| `#/admin/cust` | Customer management |
| `#/admin/ana` | Sales analytics |

---

## 📁 Current Project Structure

The current implementation is a single HTML application:

```text
Cocoa & Crumbs/
└── index.html
```

The uploaded HTML contains:

```text
HTML
├── Document structure
├── Header
├── Customer storefront
├── Product pages
├── Cart
├── Checkout
├── Wishlist
├── Admin dashboard
└── Footer

CSS
├── Theme variables
├── Responsive layout
├── Product cards
├── Buttons
├── Forms
├── Tables
├── Admin dashboard
├── Mobile navigation
└── Animations

JavaScript
├── Product seed data
├── Image generation
├── Cart state
├── Wishlist state
├── Checkout state
├── Product rendering
├── Search/filtering
├── Customer pages
├── Admin pages
├── Analytics
└── Hash router
```

---

## 🚀 Getting Started

### Option 1 — Open Directly

Because the current application is self-contained, you can open the HTML file directly in a modern browser.

1. Save the HTML as:

```text
index.html
```

2. Double-click `index.html`.

3. The Cocoa & Crumbs website will open in your browser.

### Option 2 — Use a Local Server

For a more reliable development environment, use a local HTTP server.

With Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

## 🎨 Design System

The interface uses a premium dessert-shop visual style.

### Main Colors

```text
Chocolate Brown: #3E2723
Cream:           #FBF8F1
Caramel:         #D38C41
Gold:            #D4AF37
White:           #FFFFFF
Muted Text:      #7A6A63
Border:          #EADFD0
Input Background:#F6EFE3
```

### Fonts

The current design uses:

- Playfair Display — headings and branding
- Inter — body text and UI

Fonts are loaded from Google Fonts in the HTML.

---

## 📦 Product Data

Products are generated in JavaScript for demo purposes.

The main product array is:

```javascript
const P = [];
```

Products are generated with:

```javascript
for (let i = 0; i < 200; i++) {
    // product generation
}
```

The first 100 products are chocolates.

The next 100 products are cakes.

### Product Object

A typical product follows this structure:

```javascript
{
    id: "CHO-001",
    type: "chocolate",
    name: "Product Name",
    category: "Chocolate Category",
    description: "Product description",
    price: 499,
    originalPrice: 599,
    discount: 17,
    image: "image-url",
    gallery: [],
    rating: 4.5,
    reviews: 120,
    stock: 50,
    weight: "250 g",
    ingredients: "Ingredients",
    featured: true,
    bestseller: false,
    createdAt: Date.now()
}
```

---

## 🖼️ Product Images

The current demo does not use a real 200-image product library.

Instead, it generates lightweight SVG dessert illustrations dynamically through the `art()` function.

The source code explicitly describes these images as replaceable with real URLs later.

To use real product photography, replace:

```javascript
image: art(k)
```

with a real image URL or local asset path.

For example:

```javascript
image: "/images/chocolates/belgian-dark-chocolate.jpg"
```

For production use, store product images in a dedicated asset directory or an image/CDN service.

---

## 🛒 Cart Storage

The current demo uses browser `localStorage`.

Cart data is stored under:

```text
cart
```

Wishlist data is stored under:

```text
wish
```

This allows cart and wishlist state to survive a browser refresh.

This is suitable for a demo, but a production application should store customer carts and wishlists in a backend database.

---

## 💳 Checkout

The checkout flow contains:

1. Customer details
2. Delivery address
3. Delivery option
4. Payment method
5. Order confirmation

Supported demo payment options:

- UPI
- Credit/Debit Card
- Cash on Delivery

### Important

The current payment screen is **demo-only**.

No real payment is processed.

A production deployment should integrate a secure payment gateway such as an appropriate Indian payment provider and never process raw card information directly in frontend code.

---

## 🚚 Delivery

The current demo provides:

### Standard Delivery

```text
2–3 days
```

### Express Delivery

```text
Same day
₹149
```

The product page also displays free delivery for qualifying orders.

---

## 🧾 Tax

The current cart calculation uses:

```text
5% GST
```

The exact tax treatment for a real business should be configured according to the business's applicable tax requirements.

---

## 🧑‍💼 Admin Dashboard

The admin dashboard is currently a frontend demo.

### Dashboard

Displays:

- Total products
- Chocolates
- Cakes
- Total orders
- Customers
- Today's revenue
- Monthly revenue
- Pending orders
- Low-stock products

### Products

Admins can:

- Search products
- Add products
- Edit products
- Delete products
- Update price
- Update stock
- Change category
- Mark featured
- Mark bestseller

### Orders

Admins can update order status:

```text
Pending
Confirmed
Preparing
Out for Delivery
Delivered
Cancelled
```

### Analytics

The dashboard contains demo sales charts for:

```text
Today
7 Days
30 Days
6 Months
1 Year
```

---

## 🔐 Authentication

The current demo does **not** implement real authentication or authorization.

The admin page is accessible through:

```text
#/admin
```

For production, add:

- Admin login
- Secure authentication
- Role-based access control
- Session management
- Backend authorization
- Protected API endpoints

Never rely on frontend route hiding as a security mechanism.

---

## 🗄️ Recommended Production Architecture

For a production version, the project can be migrated from the current single-file demo to:

```text
cocoa-and-crumbs/
├── app/
│   ├── page
│   ├── shop/
│   ├── products/
│   ├── cart/
│   ├── checkout/
│   └── admin/
├── components/
│   ├── Header
│   ├── Footer
│   ├── ProductCard
│   ├── ProductGrid
│   ├── Filters
│   ├── Cart
│   ├── Checkout
│   └── Dashboard
├── data/
│   └── products
├── public/
│   └── images/
│       ├── chocolates/
│       └── cakes/
├── lib/
│   └── database
├── api/
│   ├── products
│   ├── orders
│   ├── customers
│   └── payments
└── README.md
```

---

## 🧰 Recommended Production Stack

The current demo is vanilla HTML/CSS/JavaScript.

For a scalable production application, the intended architecture can use:

- Next.js
- React
- TypeScript
- Tailwind CSS
- PostgreSQL or another production database
- Secure authentication
- Cloud image storage/CDN
- Payment gateway
- Email/SMS notifications
- Server-side order processing

---

## ⚠️ Demo Limitations

The current uploaded implementation is a frontend demo and should not be treated as a production commerce backend.

Notable limitations:

- No real database
- No real authentication
- No real payment processing
- No backend API
- Demo product data is generated in JavaScript
- Product images are generated SVG illustrations
- Orders exist only in browser memory during the session
- Customer records are derived from demo orders
- Analytics are simulated
- Uploaded product images are handled as browser data
- No server-side validation
- No persistent admin database

---

## 🔧 Customization

### Change Brand Name

Search for:

```text
Cocoa & Crumbs
```

and replace it with the desired brand name.

### Change Contact Details

The current demo includes:

```text
+91 98765 43210
hello@cocoaandcrumbs.in
12 Bakers Lane, Chennai 600001
```

Replace these with the real business contact information before deployment.

### Change Theme Colors

Update the CSS variables near the top of the HTML:

```css
:root {
    --br: #3E2723;
    --cr: #FBF8F1;
    --ca: #D38C41;
    --go: #D4AF37;
}
```

### Change Product Prices

Product pricing is generated in the JavaScript seed-data section.

For real products, replace generated values with database-backed product records.

---

## 📱 Responsive Design

The application includes a mobile breakpoint at approximately:

```text
800px
```

On smaller screens:

- Desktop navigation is hidden
- Mobile bottom navigation appears
- Admin sidebar becomes horizontally scrollable
- Product layouts become single-column
- Forms become responsive
- Content spacing is reduced

---

## ♿ Accessibility Considerations

The current UI includes several accessibility-friendly features:

- Semantic buttons and links
- Image `alt` attributes on product cards
- Form labels
- Keyboard-accessible controls
- Responsive text sizing
- Visible interactive controls

Before production launch, perform a complete accessibility audit including keyboard navigation, contrast, focus states, and screen-reader testing.

---

## 📄 License

Add the project's actual license here before public distribution.

Example:

```text
MIT License
```

Do not claim a license unless one has actually been selected for the project.

---

## 📌 Project Status

**Current status:** Frontend e-commerce demo / prototype

**Product catalog:** 200 generated demo products

**Customer storefront:** Implemented

**Cart:** Implemented

**Wishlist:** Implemented

**Checkout UI:** Implemented

**Admin dashboard:** Implemented

**Real backend:** Not implemented

**Real payments:** Not implemented

**Production authentication:** Not implemented

---

## 💡 Next Development Steps

For a production-ready release, the recommended next steps are:

1. Move product data into a database.
2. Replace generated SVG images with the 200 real product images.
3. Add customer authentication.
4. Add secure admin authentication.
5. Build backend APIs.
6. Persist orders in a database.
7. Integrate a payment gateway.
8. Add real inventory management.
9. Add email/SMS order notifications.
10. Add image upload storage.
11. Add server-side validation.
12. Add deployment configuration.
13. Add automated testing.
14. Configure production environment variables.
15. Add analytics and monitoring.

---

## ❤️ Cocoa & Crumbs

**Sweet Moments. Delicious Memories.**

A premium chocolate and cake shopping experience designed for celebrations, gifting, birthdays, anniversaries, and everyday sweet moments.
