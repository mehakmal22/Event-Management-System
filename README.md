# Event-Management-System
# Event Management System

## Prerequisites

- Node.js (v20 or higher)
- Bun runtime
- PostgreSQL database (Docker container)

## Installation

1. Install Docker:

   ```bash
   # For Ubuntu/Debian
   sudo apt update
   sudo apt install docker.io docker-compose
   
   # For macOS
   brew install docker
   ```

2. Start PostgreSQL container:

   ```bash
   docker run --name postgres -e POSTGRES_PASSWORD=yourpassword -p 5432:5432 -d postgres
   ```

   Update your .env file with:
****
   ```env
   DATABASE_URL="postgresql://postgres:yourpassword@localhost:5432/postgres"
   ```

3. Install Bun:
  
   ```bash
   curl -fsSL https://bun.sh/install | bash
   ```

   For Windows users, use WSL2 to install Bun.

4. Install dependencies:

   ```bash
   bun install
   ```

5. Set up your PostgreSQL database and configure the connection URL in your environment:

   ```env
   DATABASE_URL="postgresql://username:password@localhost:5432/database_name"
   ```

6. Add any other environment variables your project needs.

7. Generate Prisma client:

   ```bash
   bun run setup:db
   ```

## Running the Project

Start the development server

