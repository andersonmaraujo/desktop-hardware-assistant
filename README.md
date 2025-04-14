# Desktop Hardware Assistant

A comprehensive API-first platform for managing, evaluating, and making decisions about desktop hardware components. This system is designed to be modular and easily integrable with third-party applications, MCP servers, and AI orchestrators.

## Project Overview

The Desktop Hardware Assistant provides a suite of services to help users:

- Manage an inventory of their desktop hardware components
- Check compatibility between components
- Receive personalized upgrade recommendations
- Monitor market prices and new hardware releases

## System Architecture

The system is built using a microservices architecture with the following components:

### Core API Gateway
- Centralized authentication and authorization
- Request routing to appropriate microservices
- Rate limiting and monitoring

### Microservices

#### Hardware Inventory Service
- Stores and manages user hardware components
- Tracks specifications, age, and performance metrics
- Provides CRUD operations for hardware inventory

#### Compatibility Service
- Rules engine for hardware compatibility checking
- Validation logic for component combinations
- Identifies potential conflicts between components

#### Recommendation Service
- System bottleneck analysis
- Upgrade path suggestions based on budget constraints
- Performance improvement estimations

#### Market Service
- Tracks component prices across retailers
- Monitors new hardware releases
- Provides historical price trend analysis

### Integration Layer
- RESTful API endpoints for all services
- GraphQL interface for complex queries
- Webhook system for event notifications

## Technical Stack

- **Backend**: FastAPI (Python)
- **Database**: MongoDB
- **Message Bus**: RabbitMQ
- **Authentication**: JWT tokens
- **Documentation**: OpenAPI/Swagger

## Getting Started

### Prerequisites

- Python 3.9+
- Docker and Docker Compose
- MongoDB
- RabbitMQ

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/andersonmaraujo/desktop-hardware-assistant.git
   cd desktop-hardware-assistant
   ```

2. Create a virtual environment and install dependencies:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   ```
   cp .env.example .env
   ```
   Edit the `.env` file with your configuration details.

4. Start the services with Docker Compose:
   ```
   docker-compose up -d
   ```

5. Access the API documentation at:
   ```
   http://localhost:8000/docs
   ```

## API Documentation

The API provides the following main endpoints:

- `/api/auth/*` - Authentication endpoints
- `/api/inventory/*` - Hardware component management
- `/api/compatibility/*` - Compatibility checking
- `/api/recommendations/*` - Upgrade recommendations
- `/api/market/*` - Price tracking and market data

Detailed API documentation is available via Swagger UI when the service is running.

## Integration Features

### Webhooks

The system provides webhooks for real-time notifications about:
- Price drops
- Compatibility issues
- New hardware releases
- Recommended upgrades

### Authentication

API access is secured with JWT tokens. Third-party applications can authenticate and receive tokens with appropriate permission scopes.

## Contributing

Contributions to the Desktop Hardware Assistant are welcome! Please refer to our [contribution guidelines](CONTRIBUTING.md) for details.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please open an issue on GitHub.