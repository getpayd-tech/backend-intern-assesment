# Payd Backend Engineering Internship Technical Assessment

## Overview
This assessment is designed to evaluate your proficiency in Golang, API design, PostgreSQL, Test Driven Development (TDD), Advanced Message Queue Protocols (AMQP), microservices architecture, and Remote Procedure Call (RPC) protocols. You will build a payment polling service that integrates with the Payd APIs to handle card and mobile payments. The assessment focuses on your ability to design, develop, and test a distributed system using modern backend technologies.

## Assessment Instructions

### Project Setup
1. **Create a new repository** on your GitHub account for this project.
2. Initialize the project with a `README.md` file containing the project overview and setup instructions.

### Services Overview
You will implement three main services:
1. **Gateway Service**: Exposes the APIs.
2. **Authentication Service**: Handles user authentication.
3. **Payments Service**: Integrates with the Payd APIs to handle payments.

### Technical Requirements
- **Languages**: Use Golang for the core services and Python for any auxiliary scripts if necessary.
- **Database**: Use PostgreSQL for data storage.
- **Message Queue**: Implement AMQP for communication between microservices.
- **Testing**: Follow Test Driven Development (TDD) principles.
- **Migration**: Use a migration tool (e.g., Golang's `migrate` library) to handle database migrations.
- **Microservices**: Design the system using a microservices architecture.
- **RPC**: Implement RPC protocols for internal service communication.

### Service Implementation Details

#### Gateway Service
**Endpoints**:
- `POST /register`: Register a new user.
- `POST /login`: Authenticate a user and return a JWT.
- `POST /payments/initiate`: Initiate a payment.
- `GET /payments/status/:id`: Poll the status of a payment.

**Tasks**:
- Expose the endpoints for user registration, login, payment initiation, and payment status polling.
- Forward authentication requests to the Authentication Service.
- Forward payment-related requests to the Payments Service.

#### Authentication Service
**Endpoints**:
- `POST /auth/register`: Register a new user.
- `POST /auth/login`: Authenticate a user and return a JWT.

**Tasks**:
- Implement user registration and authentication.
- Use JWT for securing API endpoints.
- Store user credentials securely in PostgreSQL.
- Ensure proper validation and error handling.

#### Payments Service
**Endpoints**:
- `POST /payments/initiate`: Initiate a payment.
- `GET /payments/status/:id`: Poll the status of a payment.

**Tasks**:
- Integrate with Payd APIs to initiate and poll payments.
- Use AMQP for communication with the Gateway Service.
- Store payment records in PostgreSQL.
- Implement logic for retrying failed payments and handling edge cases.

### Database and Migrations
**Tasks**:
- Design the database schema using PostgreSQL.
- Implement database migrations using a migration tool like `golang-migrate`.
- Ensure database integrity and relationships between tables.

### Additional Requirements
- **Documentation**: Provide comprehensive API documentation using Swagger or a similar tool.
- **Error Handling**: Implement robust error handling and logging mechanisms.
- **Security**: Ensure secure handling of user credentials and sensitive data.

### Submission
- Push your completed project to your GitHub repository.
- Submit your GitHub repo link to `talent@paydhq.com` including your Name and Email Address, using 'Backend Intern Submission' as the ref
- Ensure that your submission includes:
  - A brief description of your approach.
  - Any additional features or improvements you have implemented.
  - Screenshots or a demo video of your working application.
  - API documentation.

## Assessment Criteria
- **Code Quality**:
  - Clean, readable, and well-documented code.
  - Proper use of Golang best practices.
- **API Design**:
  - RESTful and intuitive API endpoints.
  - Comprehensive and clear API documentation.
- **Functionality**:
  - Correct implementation of user authentication, payment initiation, and payment status polling.
  - Proper handling of authentication and authorization.
- **Validation and Error Handling**:
  - Effective validation of input data.
  - Meaningful and user-friendly error messages.
- **Testing**:
  - Thorough unit tests covering the main functionalities.
- **Scalability and Security**:
  - Consideration of scalability and security in your implementation.

## Tips for Success
- Review the documentation for Golang and your chosen libraries to make the most of their features.
- Test your API thoroughly using tools like Postman or Insomnia.
- Consider edge cases and handle them appropriately.
- Don't hesitate to showcase your creativity and unique problem-solving skills.

The assessment is self-timed. You are expected to take the shortest time possible to deliver the most well-thought-out solution you can. Applications are reviewed on a rolling basis - the earlier you submit, the better.

Good luck! We look forward to reviewing your submission.

