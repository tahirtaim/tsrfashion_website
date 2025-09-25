# TSR Fashion App - Project Structure

This document outlines the complete project structure for the TSR Fashion App web application.

## Root Directory

```
/
├── components.json           # UI component configuration
├── docker-compose.yml        # Docker Compose configuration for containerization
├── Dockerfile                # Docker configuration for building the application image
├── next-env.d.ts             # TypeScript definitions for Next.js
├── next.config.mjs           # Next.js configuration file
├── package.json              # Project dependencies and scripts
├── postcss.config.mjs        # PostCSS configuration for CSS processing
├── README.md                 # Project documentation
├── structure.md              # This file - project structure overview
├── tailwind.config.ts        # Tailwind CSS configuration
└── tsconfig.json             # TypeScript compiler configuration
```

## Public Directory

Contains static assets served by the web server.

```
/public
├── icons/                    # SVG icons used throughout the application
│   ├── applePay.svg
│   ├── arrowLeft.svg
│   ├── arrowRight.svg
│   ├── big-star.svg
│   ├── calvin-klein-logo.svg
│   ├── cart.svg
│   ├── check.svg
│   ├── circleCheck.svg
│   ├── dotsHorizontal.svg
│   ├── envelope.svg
│   ├── facebook.svg
│   ├── github.svg
│   ├── googlePay.svg
│   ├── gucci-logo.svg
│   ├── instagram.svg
│   ├── keyboardArrowDown.svg
│   ├── keyboardArrowRight.svg
│   ├── mastercard.svg
│   ├── menu.svg
│   ├── minus.svg
│   ├── outlineOffer.svg
│   ├── paypal.svg
│   ├── plus.svg
│   ├── prada-logo.svg
│   ├── search-black.svg
│   ├── search.svg
│   ├── small-star.svg
│   ├── times.svg
│   ├── trash.svg
│   ├── user.svg
│   ├── versace-logo.svg
│   ├── verticalSlider.svg
│   ├── Visa.svg
│   ├── xTwitter.svg
│   └── zara-logo.svg
└── images/                   # Image assets used in the application
    ├── dress-style-1.png
    ├── dress-style-2.png
    ├── dress-style-3.png
    ├── dress-style-4.png
    ├── header-homepage.png
    ├── header-res-homepage.png
    ├── pic1.png
    ├── pic2.png
    ├── pic3.png
    ├── pic4.png
    ├── pic5.png
    ├── pic6.png
    ├── pic7.png
    ├── pic8.png
    ├── pic9.png
    ├── pic10.png
    ├── pic11.png
    ├── pic12.png
    ├── pic13.png
    ├── pic14.png
    └── pic15.png
```

## Source Directory

Contains the application code.

```
/src
├── app/                      # Next.js App Router directory
│   ├── favicon.ico           # Website favicon
│   ├── layout.tsx            # Root layout component
│   ├── page.tsx              # Homepage component
│   ├── providers.tsx         # App providers (Redux, etc.)
│   ├── cart/                 # Cart page
│   │   └── page.tsx
│   └── shop/                 # Shop page
│       ├── page.tsx
│       └── product/          # Product page directory
├── components/               # React components organized by feature
│   ├── cart-page/            # Cart page components
│   │   ├── BreadcrumbCart.tsx
│   │   └── ProductCard.tsx
│   ├── common/               # Shared components used across pages
│   │   ├── ProductCard.tsx
│   │   ├── ProductListSec.tsx
│   │   └── ReviewCard.tsx
│   ├── homepage/             # Homepage components
│   │   ├── Brands/
│   │   ├── DressStyle/
│   │   ├── Header/
│   │   └── Reviews/
│   ├── layout/               # Layout components
│   │   ├── Banner/
│   │   ├── Footer/
│   │   └── Navbar/
│   ├── product-page/         # Product page components
│   │   ├── BreadcrumbProduct.tsx
│   │   ├── Header/
│   │   └── Tabs/
│   ├── shop-page/            # Shop page components
│   │   ├── BreadcrumbShop.tsx
│   │   └── filters/
│   ├── storage/              # Storage related components
│   │   └── index.tsx
│   └── ui/                   # UI components library
│       ├── accordion.tsx
│       ├── AnimatedCounter.tsx
│       ├── breadcrumb.tsx
│       ├── button.tsx
│       ├── carousel.tsx
│       ├── CartCounter.tsx
│       ├── drawer.tsx
│       ├── input-group.tsx
│       ├── navigation-menu.tsx
│       ├── pagination.tsx
│       ├── Rating.tsx
│       ├── select.tsx
│       ├── separator.tsx
│       ├── sheet.tsx
│       ├── slider copy.tsx
│       ├── slider.tsx
│       └── SpinnerbLoader/
├── lib/                      # Utility libraries and state management
│   ├── store.ts              # Redux store configuration
│   ├── utils.ts              # Utility functions
│   ├── features/             # Redux features/slices
│   │   ├── carts/            # Cart related state management
│   │   └── products/         # Products related state management
│   └── hooks/                # Custom React hooks
│       └── redux.tsx         # Redux hooks
├── styles/                   # Global styles
│   ├── globals.css           # Global CSS styles
│   └── fonts/                # Font assets
│       └── index.ts          # Font exports
└── types/                    # TypeScript type definitions
    ├── product.types.ts      # Product related types
    └── review.types.ts       # Review related types
```

## Application Structure

### Frontend Framework

- **Next.js**: React framework with server-side rendering capabilities
- **TypeScript**: Strongly-typed programming language

### Styling

- **Tailwind CSS**: Utility-first CSS framework
- **PostCSS**: CSS transformation tool

### State Management

- **Redux**: State management library
  - Organized in features (carts, products)
  - Custom hooks for accessing Redux state

### UI Components

The project uses a component-based architecture with:
- Page-specific components (homepage, cart-page, product-page, shop-page)
- Common components shared across pages
- Layout components (Banner, Footer, Navbar)
- UI primitives (button, carousel, sheet, etc.)

### Docker Support

The application includes Docker configuration for containerized deployment:
- `Dockerfile`: Container image definition
- `docker-compose.yml`: Multi-container orchestration

### Asset Management

Assets are organized in the public directory:
- Icons: SVG format for scalability
- Images: Product photos and UI images

### TypeScript Integration

The project uses TypeScript for type safety with:
- Custom type definitions in `/src/types`
- Next.js type definitions
- TypeScript configuration in tsconfig.json