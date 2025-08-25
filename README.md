# airbnb-clone-project

## Team Roles

- **Backend Developer**: Builds APIs, server logic, ensures security and performance.  
- **Database Administrator**: Manages databases, ensures data integrity, backups, and optimization.  
- **Frontend Developer**: Develops user interface, integrates with APIs, ensures responsiveness.  
- **Project Manager**: Plans tasks, manages timelines, ensures communication and delivery.  
- **QA Engineer**: Tests features, finds bugs, ensures overall product quality.  
- **DevOps Engineer**: Handles deployment, CI/CD, cloud infrastructure, and monitoring.  
- **UX/UI Designer**: Designs user-friendly interfaces and improves user experience.  


## Technology Stack

- **Django**: Web framework for building backend services and RESTful APIs.  
- **PostgreSQL**: Relational database used to store and manage structured data.  
- **GraphQL**: Query language that allows clients to request only the data they need.  
- **Docker**: Containerization tool to package and deploy applications consistently.  
- **Git & GitHub**: Version control and collaboration platform for source code management.  
- **CI/CD (GitHub Actions)**: Automates testing, integration, and deployment pipelines.  


## Database Design

### Key Entities & Fields

- **Users**: `id`, `name`, `email`, `password`, `role`  
- **Properties**: `id`, `title`, `description`, `location`, `owner_id`  
- **Bookings**: `id`, `user_id`, `property_id`, `start_date`, `end_date`  
- **Reviews**: `id`, `user_id`, `property_id`, `rating`, `comment`  
- **Payments**: `id`, `booking_id`, `amount`, `status`, `payment_date`  

### Relationships
- A **User** can own multiple **Properties**.  
- A **User** can make multiple **Bookings**.  
- A **Booking** belongs to one **Property** and one **User**.  
- A **Review** is written by a **User** for a **Property**.  
- A **Payment** is linked to one **Booking**.  


## Feature Breakdown

### 1. User Management
Allows users to register, log in, and manage their profiles. Provides authentication and authorization to secure the platform and personalize user experiences.  

### 2. Property Management
Hosts can list new properties with details such as title, description, location, and price. They can also update or remove their listings as needed.  

### 3. Booking System
Enables guests to book available properties for specific dates. Manages availability, prevents double bookings, and links bookings to users and properties.  

### 4. Review System
Users can leave reviews and ratings for properties they have booked. This helps build trust and improves the decision-making process for future guests.  

### 5. Payment Processing
Handles secure payments for bookings, including tracking payment status. Ensures transactions are reliable and linked directly to bookings.  

### 6. Search & Filter
Provides search functionality by location, date, and price. Filtering options improve user experience by helping guests find properties that match their needs.  


## API Security

### Key Security Measures

- **Authentication**: Ensures only registered users can access protected endpoints, protecting sensitive data.  
- **Authorization**: Controls what actions each user can perform (e.g., only property owners can edit their listings).  
- **Rate Limiting**: Prevents abuse and denial-of-service attacks by limiting the number of requests per user/IP.  
- **Data Validation & Sanitization**: Prevents malicious input and protects against SQL/NoSQL injection attacks.  
- **Secure Payment Handling**: Ensures payment data is processed safely and users’ financial information is protected.  


## CI/CD Pipeline

Continuous Integration and Continuous Deployment (CI/CD) automates testing, building, and deploying the application. It ensures that new code changes are integrated smoothly and deployed quickly, reducing errors and improving reliability.  

**Tools Used:** GitHub Actions for automation, Docker for containerization, and optional cloud platforms for deployment.

