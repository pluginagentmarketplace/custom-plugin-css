---
name: frameworks-databases
description: Master modern web frameworks (React, Vue, Angular, Node.js, Spring Boot) and database technologies (SQL, MongoDB, Redis, GraphQL). Build complete full-stack applications with industry-standard tools. Use when learning frameworks, databases, or building full-stack applications.
---

# Frameworks & Databases Skill

## Quick Start

### React Application Setup
```javascript
// Modern React with Hooks
import { useState, useEffect } from 'react';

function App() {
    const [data, setData] = useState(null);
    const [loading, setLoading] = useState(true);

    useEffect(() => {
        fetchData();
    }, []);

    const fetchData = async () => {
        try {
            const response = await fetch('/api/data');
            const result = await response.json();
            setData(result);
        } finally {
            setLoading(false);
        }
    };

    return loading ? <div>Loading...</div> : <div>{data}</div>;
}
```

### Express.js Backend
```javascript
const express = require('express');
const app = express();

app.use(express.json());

app.get('/api/data', (req, res) => {
    res.json({ message: 'Hello' });
});

app.post('/api/data', (req, res) => {
    const newData = req.body;
    // Process data
    res.status(201).json(newData);
});

app.listen(3000, () => console.log('Server started'));
```

### SQL Query Patterns
```sql
-- CRUD Operations
SELECT * FROM users WHERE id = 1;
INSERT INTO users (name, email) VALUES ('John', 'john@example.com');
UPDATE users SET email = 'new@example.com' WHERE id = 1;
DELETE FROM users WHERE id = 1;

-- Joins
SELECT u.name, o.total
FROM users u
LEFT JOIN orders o ON u.id = o.user_id;

-- Aggregation
SELECT category, COUNT(*) as count, AVG(price) as avg_price
FROM products
GROUP BY category;
```

## Frontend Framework Patterns

### React Ecosystem
- **Hooks:** useState, useEffect, useContext, useReducer
- **State Management:** Redux, Zustand, Context API, Recoil
- **Routing:** React Router v6+
- **Testing:** Jest, React Testing Library
- **Performance:** Code splitting, memoization, lazy loading

### Vue 3
- **Composition API:** ref(), reactive(), computed()
- **State Management:** Pinia, Vuex
- **Routing:** Vue Router
- **Component Patterns:** Scoped slots, render functions
- **Developer Experience:** HMR, debugging

### Angular
- **Services & Dependency Injection:** Provider pattern
- **RxJS:** Observables, operators, async pipe
- **Forms:** Reactive & template-driven
- **HTTP Client:** Interceptors, error handling
- **Performance:** OnPush change detection

## Backend Framework Patterns

### Express.js
- **Middleware:** Authentication, logging, error handling
- **Routing:** REST endpoints, middleware chains
- **Templating:** EJS, Pug, Handlebars
- **Error Handling:** Global error handlers
- **Security:** CORS, helmet, rate limiting

### Spring Boot
- **Annotations:** @Controller, @Service, @Repository
- **Dependency Injection:** ApplicationContext, bean management
- **JPA/Hibernate:** ORM, entity mapping
- **REST Controllers:** @GetMapping, @PostMapping, content negotiation
- **Security:** Spring Security, JWT, OAuth2

### ASP.NET Core
- **Dependency Injection:** Built-in DI container
- **Middleware:** Pipeline, custom middleware
- **Entity Framework:** ORM, migrations, LINQ
- **API Controllers:** Routing, model binding
- **Authentication:** Identity, OAuth2, API keys

## Database Patterns

### Relational Databases (SQL)
- **Schema Design:** Normalization, relationships
- **Indexing:** Query optimization, B-tree indexes
- **Transactions:** ACID properties, isolation levels
- **Joins:** INNER, LEFT, RIGHT, FULL joins
- **Aggregation:** GROUP BY, HAVING, window functions

### NoSQL (MongoDB)
- **Collections & Documents:** Flexible schema
- **Queries:** Query operators, aggregation pipeline
- **Indexing:** Single field, compound indexes
- **Replication:** Replica sets, high availability
- **Sharding:** Horizontal scaling

### Caching (Redis)
- **Data Types:** Strings, Lists, Sets, Hashes, Sorted Sets
- **Expiration:** TTL, eviction policies
- **Pub/Sub:** Message brokers, real-time features
- **Transactions:** MULTI, EXEC, WATCH
- **Persistence:** RDB, AOF

### GraphQL
- **Schema Definition:** Types, fields, mutations
- **Resolvers:** Field resolution, async handling
- **Queries & Mutations:** Request structure
- **Subscriptions:** Real-time updates
- **Middleware:** Permissions, logging, caching

## Full-Stack Integration Patterns

### API Design
```javascript
// RESTful endpoints
GET    /api/v1/users           # List all
POST   /api/v1/users           # Create
GET    /api/v1/users/:id       # Get one
PUT    /api/v1/users/:id       # Update
DELETE /api/v1/users/:id       # Delete

// Response format
{
    "status": "success",
    "data": { ... },
    "meta": {
        "page": 1,
        "total": 100,
        "limit": 10
    }
}
```

### Authentication Flow
1. User submits credentials
2. Backend validates & creates JWT
3. Token stored in httpOnly cookie/localStorage
4. Client sends token with requests
5. Server validates token & request proceeds
6. Token refreshed before expiration

### Data Validation
- **Frontend:** Client-side validation for UX
- **Backend:** Server-side validation for security
- **Database:** Constraints & triggers
- **API:** Schema validation (Joi, Zod, Yup)

## Performance Optimization

### Frontend
- Code splitting & lazy loading
- Memoization (React.memo, useMemo)
- Image optimization (WebP, AVIF)
- CSS-in-JS tree shaking
- Bundle size analysis

### Backend
- Database indexing
- Query optimization
- Caching strategies (Redis)
- Pagination for large datasets
- Connection pooling

### Full-Stack
- CDN for static assets
- Compression (gzip, brotli)
- HTTP/2 multiplexing
- Service workers
- Edge caching

## Security Best Practices

### Application Security
- Input validation
- CSRF protection
- XSS prevention
- SQL injection protection
- Rate limiting

### Data Protection
- Password hashing (bcrypt)
- SSL/TLS encryption
- Secrets management
- Audit logging
- Data encryption at rest

## Common Tech Stack Combinations

### MERN (MongoDB, Express, React, Node)
- Full JavaScript stack
- JSON throughout
- Flexible schema
- Great for startups

### MEAN (MongoDB, Express, Angular, Node)
- Enterprise ready
- TypeScript first
- Opinionated structure
- Built-in features

### Spring Boot + React + PostgreSQL
- Java backend
- Modern frontend
- Relational database
- Enterprise scale

### Next.js + GraphQL
- Full-stack framework
- Server-side rendering
- Type-safe API
- Built-in optimization

## When to Use This Skill

### Framework Selection
- Learning a new framework
- Building a specific feature
- Understanding architecture patterns
- Migrating between frameworks
- Evaluating technology choices

### Database Selection
- Choosing between SQL/NoSQL
- Scaling considerations
- Query pattern requirements
- Consistency vs availability
- Cost optimization

## Resources

- **Official Documentation** - Framework & DB docs
- **Tutorial Projects** - Full-stack examples
- **GitHub Examples** - Real-world code
- **Performance Tools** - Lighthouse, DevTools
- **Security Guides** - OWASP, framework security docs
