# Sports Club Booking & Management System

A comprehensive web-based platform for managing multiple sports club branches across cities, providing centralized booking, facility management, and reporting capabilities.

## 🏆 Project Overview

This system streamlines sports club operations by providing:
- **Multi-branch Management**: Support for sports clubs with multiple locations
- **Real-time Booking**: Instant booking confirmation and availability checking
- **Role-based Access**: Different access levels for members, admins, and super admins
- **Comprehensive Reporting**: Analytics and data export capabilities
- **Responsive Design**: Mobile-friendly interface for all devices

## 🛠️ Technology Stack

### Backend
- **Framework**: Spring Boot 3.x with Spring MVC
- **Architecture**: Domain-Driven Design (DDD) with Clean Architecture
- **Database**: MySQL 8.0+
- **Authentication**: JWT with Spring Security
- **API**: RESTful APIs with OpenAPI documentation

### Frontend
- **Framework**: React.js 18+
- **UI Library**: Material-UI / Tailwind CSS
- **State Management**: Context API / Redux Toolkit
- **Build Tool**: Vite

### Infrastructure
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Monitoring**: Spring Boot Actuator with Prometheus/Grafana
- **Email Service**: SMTP integration

## 📋 Features

### Core Features
- ✅ User registration and authentication
- ✅ Multi-branch facility management
- ✅ Real-time slot booking system
- ✅ Booking management (create, reschedule, cancel)
- ✅ Role-based access control
- ✅ Email notifications
- ✅ Comprehensive reporting and analytics
- ✅ Data export (CSV/Excel)

### User Roles
- **Member**: Book facilities, manage bookings, view history
- **Admin**: Manage branch facilities, slots, and bookings
- **Super Admin**: Full system access, multi-branch management

## 🏗️ Architecture

### Domain-Driven Design Structure
```
src/
├── main/java/com/sportclub/
│   ├── api/              # Controllers and DTOs
│   ├── application/      # Services and Use Cases
│   ├── domain/           # Business Logic
│   │   ├── user/         # User Aggregate
│   │   ├── booking/      # Booking Aggregate
│   │   ├── facility/     # Facility Aggregate
│   │   └── branch/       # Branch Aggregate
│   └── infrastructure/   # Data Access and External Services
```

### Key Business Rules
- Maximum 2 bookings per user per day
- Minimum 2 hours advance booking
- 24-hour cancellation policy
- 15-minute buffer between bookings

## 📊 Database Schema

### Core Tables
- `users` - User accounts and authentication
- `branches` - Branch locations and details
- `facilities` - Facility information per branch
- `slots` - Time slot definitions
- `bookings` - Booking records and status
- `branch_admins` - Admin-to-branch assignments

## 🚀 Getting Started

### Prerequisites
- Java 17+
- Node.js 18+
- MySQL 8.0+
- Maven 3.9+

### Installation

1. Clone the repository
```bash
git clone https://github.com/sanjayzen/sports-club-booking-mgmt.git
cd sports-club-booking-mgmt
```

2. Set up the database
```bash
# Create database
mysql -u root -p
CREATE DATABASE sports_club_db;
```

3. Configure application properties
```bash
# Copy and edit application.yml
cp src/main/resources/application-example.yml src/main/resources/application.yml
```

4. Run the backend
```bash
./mvnw spring-boot:run
```

5. Run the frontend
```bash
cd frontend
npm install
npm start
```

## 📖 Documentation

### Project Documentation
- [Functional Requirements](docs/confluence-functional-requirements.md)
- [Technical Architecture](docs/confluence-technical-requirements.md)
- [User Stories](docs/confluence-user-stories.md)
- [Architecture Diagrams](docs/confluence-architecture-diagrams.md)

### API Documentation
- Swagger UI: `http://localhost:8080/swagger-ui.html`
- OpenAPI Spec: `http://localhost:8080/v3/api-docs`

## 🧪 Testing

### Run Tests
```bash
# Backend tests
./mvnw test

# Frontend tests
cd frontend
npm test

# Integration tests
./mvnw test -Dtest=*IntegrationTest
```

### Test Coverage
- Unit Tests: 80% minimum coverage
- Integration Tests: 70% minimum coverage
- End-to-End Tests: Critical user journeys

## 🔧 Development Guidelines

### Code Standards
- Follow Domain-Driven Design principles
- Use conventional commits specification
- Maintain clean architecture layers
- Write comprehensive unit tests

### Commit Convention
```
feat(scope): add new feature
fix(scope): fix issue
docs(scope): update documentation
test(scope): add tests
refactor(scope): refactor code
```

## 🚢 Deployment

### Docker Deployment
```bash
# Build images
docker-compose build

# Start services
docker-compose up -d
```

### Production Deployment
- Use Docker containers
- Configure environment variables
- Set up database migrations
- Configure SSL certificates

## 📈 Performance Requirements

- Support 1000+ concurrent users
- API response time < 500ms (95th percentile)
- 99.9% uptime availability
- Database query optimization with proper indexing

## 🔒 Security Features

- HTTPS encryption for all communications
- JWT token-based authentication
- Role-based access control (RBAC)
- Input validation and sanitization
- SQL injection prevention
- XSS protection
- Rate limiting (100 requests/minute per user)

## 📊 Project Statistics

- **Total Story Points**: 162
- **Epics**: 5 major functional areas
- **User Stories**: 18 detailed stories
- **Functional Requirements**: 66 specific requirements
- **Estimated Timeline**: 12-16 weeks

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support and questions:
- Create an issue in the GitHub repository
- Contact the development team
- Review the documentation in the `/docs` folder

## 🎯 Roadmap

### Phase 1 (Weeks 1-4)
- ✅ User Management System
- ✅ Branch Management System

### Phase 2 (Weeks 5-8)
- 🔄 Facility Management System
- 🔄 Booking Management System

### Phase 3 (Weeks 9-12)
- 📊 Reporting & Analytics System
- 📧 Email Notifications

### Phase 4 (Weeks 13-16)
- 🧪 Testing & Quality Assurance
- 🚀 Production Deployment

## 📋 Epic Breakdown

### Epic 1: User Management (21 Story Points)
- User Registration & Authentication
- Profile Management
- Password Reset Functionality

### Epic 2: Branch Management (16 Story Points)
- Branch CRUD Operations
- Branch Analytics Dashboard

### Epic 3: Facility Management (39 Story Points)
- Facility CRUD Operations
- Slot Management
- Availability Configuration

### Epic 4: Booking Management (47 Story Points)
- Booking Search & Creation
- Booking Modifications
- Booking History

### Epic 5: Reporting & Analytics (39 Story Points)
- Data Export Functionality
- Admin Dashboards
- Performance Reports

---

**Repository**: [sports-club-booking-mgmt](https://github.com/sanjayzen/sports-club-booking-mgmt)  
**Author**: Development Team  
**Version**: 1.0  
**Status**: In Development