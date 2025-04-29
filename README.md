# AirBnB Clone Project

A full-stack booking platform clone built with **React (TypeScript), Next.js, and Django**. This project emphasizes UI/UX best practices, component reusability, and team collaboration.

---

## UI Component Patterns

Reusable components to ensure consistency and scalability:

| Component       | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| **Navbar**      | Responsive navigation with search, user auth links, and mobile menu toggle. |
| **Property Card** | Displays property image, title, price, and ratings in a grid layout.       |
| **Booking Modal** | Date picker, guest selector, and price calculator for reservations.        |
| **Footer**      | Multi-column layout with links, copyright, and social media icons.          |

---

## Project Roles and Responsibilities

| Role                  | Key Responsibilities                                                                 |
|-----------------------|-------------------------------------------------------------------------------------|
| **Project Manager**   | Oversees timelines, resource allocation, and stakeholder communication.              |
| **Frontend Devs**     | Implements React components, integrates APIs, and ensures responsive design.        |
| **Backend Devs**      | Develops Django APIs, manages databases, and handles authentication.                |
| **Designers**         | Creates Figma mockups, defines typography/colors, and ensures UI consistency.        |
| **QA/Testers**        | Writes test cases, performs manual/automated testing, and tracks bugs.              |
| **DevOps Engineers**  | Configures CI/CD pipelines, deploys to cloud platforms, and monitors performance.    |
| **Product Owner**     | Prioritizes features, manages backlog, and aligns development with business goals.  |
| **Scrum Master**      | Facilitates Agile ceremonies (stand-ups, retrospectives) and removes blockers.       |

---

## UI/UX Design Planning

### Design Goals
1. **User-Friendly Flow**: Intuitive navigation from browsing to booking.  
2. **Visual Consistency**: Cohesive colors, typography, and spacing.  
3. **Accessibility**: WCAG-compliant contrast and keyboard navigation.  

### Key Features
| Page                  | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| **Property Listing**  | Grid of property cards with filters (price, location, amenities).           |
| **Detailed View**     | High-res images, amenity icons, interactive map, and booking widget.        |
| **Checkout View**     | Minimalist form with date picker, price summary, and payment gateway.       |

### Design Properties
- **Colors**:  
  - Primary: `#FF5A5F` (AirBnB-inspired coral)  
  - Secondary: `#008489` (teal for accents)  
  - Neutral: `#F7F7F7` (light gray background)  
- **Typography**:  
  - Font Family: `Inter` (sans-serif)  
  - Headings: `600` weight, `24px–32px` size  
  - Body Text: `400` weight, `16px` size  

**Why It Matters**:  
Identifying these properties early ensures design consistency across components and avoids redundant styling efforts.

---

## Importance of User-Friendly Design
A booking system's success hinges on:  
1. **Reduced Friction**: Clear CTAs (e.g., "Book Now") and minimal form fields.  
2. **Trust Signals**: High-quality images, reviews, and transparent pricing.  
3. **Mobile Optimization**: 50%+ users book via mobile devices.  

---

## Getting Started
```bash
git clone https://github.com/r-repo/airbnb-clone.git
cd frontend && npm install
cd ../backend && pip install -r requirements.txt
