# AirBnB Clone Project

A full-stack booking platform clone built with **React (TypeScript), Next.js, and Django**. This project emphasizes UI/UX best practices, component reusability, and team collaboration.

---

## Project Roles and Responsibilities

| Role                      | Responsibilities                                                                 |
|---------------------------|---------------------------------------------------------------------------------|
| **Project Manager**       | Oversees timelines, resource allocation, and stakeholder communication.         |
| **Frontend Developer**    | Builds responsive UIs with React, implements state management, and consumes APIs.|
| **Backend Developer**     | Implements RESTful APIs, handles business logic, and integrates with databases. |
| **Database Administrator**| Designs schema, optimizes queries, and ensures data integrity and security.     |
| **UI/UX Designer**        | Creates wireframes, prototypes, and maintains design system consistency.        |
| **QA Engineer**           | Develops test plans, performs automated testing, and ensures bug-free releases. |
| **DevOps Engineer**       | Manages CI/CD pipelines, cloud infrastructure, and deployment automation.       |
| **Product Owner**         | Defines requirements, prioritizes features, and validates business value.       |
| **Scrum Master**          | Facilitates Agile ceremonies and removes team impediments.                      |

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

## Database Design

### Key Entities

| Entity      | Important Fields                          | Relationships                              |
|-------------|-------------------------------------------|--------------------------------------------|
| **Users**   | `id`, `email`, `password_hash`, `role`    | One-to-many with Properties and Bookings   |
| **Properties** | `id`, `title`, `price`, `location`, `owner_id` | Many-to-one with Users, one-to-many with Bookings |
| **Bookings** | `id`, `property_id`, `user_id`, `dates`, `total_price` | Many-to-one with Users and Properties |
| **Reviews** | `id`, `property_id`, `user_id`, `rating`, `comment` | Many-to-one with Users and Properties |
| **Payments** | `id`, `booking_id`, `amount`, `status`, `method` | One-to-one with Bookings              |

---

## Feature Breakdown

### Core Features

| Feature               | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| **User Management**   | Handles registration, authentication, and profile management (JWT auth).    |
| **Property Management** | Allows hosts to create/update listings with images and amenities.          |
| **Booking System**    | Enables date selection, availability checks, and reservation processing.    |
| **Search & Filters**  | Location-based search with price/amenity filters using geospatial queries.  |
| **Review System**     | Lets guests rate properties and leave feedback (1-5 stars + comments).      |

---

## UI/UX Design Planning

### Design Goals
1. **User-Friendly Flow**: Intuitive navigation from browsing to booking.  
2. **Visual Consistency**: Cohesive colors, typography, and spacing.  
3. **Accessibility**: WCAG-compliant contrast and keyboard navigation.  

### Key Pages
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

## API Security

### Key Measures
1. **Authentication**  
   - JWT tokens with short expiration times  
   - Why: Prevents unauthorized access to user accounts  

2. **Authorization**  
   - Role-based access control (RBAC)  
   - Why: Ensures hosts can't modify others' properties  

3. **Rate Limiting**  
   - 100 requests/minute per IP via Nginx  
   - Why: Prevents brute force/DDoS attacks  

4. **Data Validation**  
   - Input sanitization + prepared statements  
   - Why: Blocks SQL injection and XSS attacks  

5. **Payment Security**  
   - PCI-compliant Stripe integration  
   - Why: Protects sensitive financial data  

---

