# Product Showcase Website

A Hugo-based website to showcase products across 3 main categories: Electronics, Clothing, and Sports & Fitness.

## Structure

### Content Organization
```
content/
├── _index.md                    # Homepage content
├── products/
│   ├── _index.md               # Main products page
│   ├── electronics/
│   │   ├── _index.md          # Electronics category page
│   │   ├── smartphone.md      # Sample product
│   │   └── laptop.md          # Sample product
│   ├── clothing/
│   │   ├── _index.md          # Clothing category page
│   │   └── designer-jacket.md # Sample product
│   ├── home-garden/
│   │   ├── _index.md          # Home & Garden category page
│   │   └── smart-lamp.md      # Sample product
│   └── sports/
│       ├── _index.md          # Sports & Fitness category page
│       └── yoga-mat.md        # Sample product
```

### Layouts
```
layouts/
├── index.html                 # Custom homepage layout
└── products/
    ├── list.html              # Product category listing layout
    └── single.html             # Individual product detail layout
```

## Adding New Products

To add a new product:

1. Create a new markdown file in the appropriate category folder (e.g., `content/products/electronics/new-product.md`)
2. Add front matter with product details:
```yaml
---
title: "Product Name"
description: "Product description"
price: "$99"
image: "/images/product-image.jpg"
category: "electronics"
date: 2024-01-15
---
```

3. Add product content below the front matter

## Adding New Categories

To add a new product category:

1. Create a new folder under `content/products/` (e.g., `content/products/new-category/`)
2. Create an `_index.md` file in that folder with category details
3. Update the homepage layout (`layouts/index.html`) to include the new category

## Running the Website

### Development Server
```bash
cd quickstart
hugo server --buildDrafts
```

### Production Build
```bash
cd quickstart
hugo
```

The built site will be in the `public/` folder.

## Customization

### Site Configuration
Edit `hugo.toml` to change:
- Site title and description
- Base URL
- Theme settings
- Custom parameters

### Styling
The site uses the Ananke theme. You can override styles by:
1. Adding custom CSS to `assets/css/`
2. Modifying the theme colors in `hugo.toml`
3. Creating custom layout templates in `layouts/`

### Images
Add product images to the `static/images/` folder and reference them in the product front matter.

## Features

- ✅ Homepage with 3 product category sections
- ✅ Product category listing pages
- ✅ Individual product detail pages
- ✅ Responsive design (mobile-friendly)
- ✅ Key Products section
- ✅ Clean, modern interface
- ✅ Easy product management through markdown files

## Deployment

The static site in the `public/` folder can be deployed to:
- Netlify
- Vercel
- GitHub Pages
- Any static hosting service
