# HireLink (Backend)

HireLink is a robust and modern backend API designed for a recruitment and hiring platform. It bridges the gap between **Talents** (job seekers) and **Employers** by facilitating job postings, applications, and profile management.

Built with **Node.js** and **Express**, this project focuses on performance, security, and scalability, utilizing **Prisma** for database management and **Zod** for strictly typed validation.

> **Note**: This repository is a **graduation project** intended for learning and demonstration. While it implements real-world patterns like RBAC, Auth, and Validation, certain production-grade complexities (like full TypeScript adoption or OpenAPI pipelines) were intentionally scoped out.

## 🚀 Key Features

*   **Authentication & Authorization**: Secure user authentication using JWT and customized Role-Based Access Control (RBAC) for generic users, talents, employers, and moderators.
*   **Job Management**: Full CRUD operations for job postings, including categorization and search capabilities.
*   **Application System**: streamlined workflow for talents to apply for jobs and for employers to track applications.
*   **Profile Management**: Dedicated routes for Talents and Employers to manage their professional profiles.
*   **Moderation Tools**: Admin capabilities to oversee platform activity and content.
*   **File Handling**: Integration with **Cloudinary** for secure and efficient image/document storage (e.g., resumes, avatars).
*   **Security First**: Implements **Helmet**, **Rate Limiting**, **HPP**, and **CORS** best practices.
*   **Email Notifications**: Integrated **Nodemailer** for transactional emails.

## 🛠️ Tech Stack

*   **Runtime**: [Node.js](https://nodejs.org/) (v24+)
*   **Framework**: [Express.js](https://expressjs.com/) (v5)
*   **Database**: [PostgreSQL](https://www.postgresql.org/)
*   **ORM**: [Prisma](https://www.prisma.io/)
*   **Validation**: [Zod](https://zod.dev/)
*   **Testing**: [Vitest](https://vitest.dev/) & [Supertest](https://github.com/ladjs/supertest)
*   **Logging**: [Pino](https://github.com/pinojs/pino)
*   **Tooling**: [Biome](https://biomejs.dev/) (Linting & Formatting)

## 📦 Installation & Setup

1.  **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/hirelink-backend.git
    cd hirelink-backend
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Environment Variables**
    Create a `.env` file in the root directory based on `.env.example`:
    ```bash
    cp .env.example .env
    ```
    *Ensure you configure your PostgreSQL connection string, JWT secrets, and Cloudinary credentials.*

4.  **Database Setup**
    Run Prisma migrations to set up your database schema:
    ```bash
    npm run prisma:migrate
    # Optional: Seed the database with initial data
    npm run prisma:seed
    ```

5.  **Run the Server**
    *   **Development**:
        ```bash
        npm run dev
        ```
    *   **Production**:
        ```bash
        npm start
        ```

## 🧪 Testing

Run the comprehensive test suite using Vitest:

```bash
npm test
```

## 📂 Project Structure

*   `src/controllers` - Request handlers (logic)
*   `src/routes` - API route definitions
*   `src/services` - Business logic and database interactions
*   `src/middleware` - Auth, validation, and error handling middleware
*   `src/validators` - Zod schemas for input validation
*   `prisma/schema.prisma` - Database schema definition

---

*This project was developed as part of a graduation requirement.*
