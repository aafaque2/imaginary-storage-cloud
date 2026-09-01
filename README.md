# ImaginaryStore

A comprehensive file upload and storage solution with a modern web interface, powerful backend API, and embeddable JavaScript widget for seamless file management across web applications.

## 🚀 Project Overview

ImaginaryStorage is a full-stack file storage platform designed to simplify file upload, management, and sharing for modern web applications. The project consists of multiple interconnected applications that work together to provide a complete file storage ecosystem.

### Current Status

✅ **Completed Components:**
- **Backend API** - Full-featured NestJS backend with authentication, file management, and storage providers
- **Frontend Dashboard** - React-based web interface for file management and user administration
- **Upload Widget** - Embeddable JavaScript widget for easy integration into any web application
- **Landing Site** - Marketing site with comprehensive documentation
- **Proxy Service** - Secure file serving with authentication and access control

🚧 **In Development:**
- Enhanced storage provider integrations
- Advanced file processing capabilities
- Improved user management and permissions

## 🎯 Project Goals

### Current Goals
- Provide a complete, production-ready file storage solution
- Support multiple cloud storage providers (AWS S3, Google Cloud Storage)
- Offer seamless integration with existing web applications
- Maintain high security standards with proper authentication and access controls
- Deliver excellent developer experience with comprehensive documentation

### Future Goals
- **Local Filesystem Support** - Add support for local file storage for self-hosted deployments
- **Additional Storage Providers** - Integrate with more cloud storage services (Azure Blob, DigitalOcean Spaces, etc.)
- **Enhanced File Processing** - Image optimization, video transcoding, document conversion
- **Advanced Collaboration** - File sharing, commenting, and collaborative editing features
- **Mobile SDKs** - Native mobile SDKs for iOS and Android applications
- **Enterprise Features** - Advanced user management, audit logs, compliance features

## 📁 Project Structure

```
imaginary-store/
├── 📁 apps/                          # Application modules
│   ├── 📁 frontend/                  # React dashboard application
│   │   ├── src/components/           # React components
│   │   ├── src/api/                  # API client and hooks
│   │   ├── src/stores/               # State management
│   │   └── package.json
│   │
│   ├── 📁 nest-backend/              # NestJS API server
│   │   ├── src/modules/              # Feature modules
│   │   │   ├── auth/                 # Authentication & authorization
│   │   │   ├── files/                # File management
│   │   │   ├── storage/              # Storage provider integrations
│   │   │   ├── upload/               # File upload handling
│   │   │   └── users/                # User management
│   │   ├── src/schemas/              # Database schemas
│   │   └── package.json
│   │
│   ├── 📁 imaginary-widget/          # Embeddable upload widget
│   │   ├── src/core/                 # Core widget functionality
│   │   ├── src/ui/                   # User interface components
│   │   ├── src/api/                  # Widget API client
│   │   ├── dist/                     # Built widget files
│   │   └── package.json
│   │
│   ├── 📁 landing-site/              # Marketing & documentation site
│   │   ├── src/app/                  # Next.js app router
│   │   ├── src/components/           # Site components
│   │   ├── src/app/docs/             # MDX documentation
│   │   └── package.json
│   │
│   └── 📁 proxy/                     # File serving proxy
│       ├── src/adapters/             # Storage adapter implementations
│       ├── src/auth/                 # Authentication middleware
│       └── package.json
│
├── 📁 deploy/                        # Deployment configurations
│   ├── docker-compose.yml            # Production deployment
│   ├── docker-compose.local.yml      # Local development
│   └── config/nginx/                 # Nginx configurations
│
├── 📁 scripts/                       # Utility scripts
│   ├── run-all.sh                    # Start all services
│   └── add-todo.sh                   # Development utilities
│
├── 📁 journal/                       # Development documentation
│   ├── implementations/              # Implementation notes
│   ├── issues/                       # Known issues and solutions
│   └── plans/                        # Development planning
│
├── 📁 todo/                          # Task management
│
├── package.json                      # Root package.json
└── README.md                         # This file
```

## 🛠️ Getting Started

### Prerequisites

Ensure you have the following installed:
- **Node.js** 18+ 
- **npm** 9+
- **MongoDB** (for backend database)
- **Redis** (for caching and sessions)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-org/imaginary-store.git
   cd imaginary-store
   ```

2. **Install all dependencies**
   ```bash
   npm install
   ```

3. **Start all services in development mode**
   ```bash
   npm run dev
   ```

   This will start:
   - **Frontend Dashboard**: http://localhost:3000
   - **Backend API**: http://localhost:3001
   - **Landing Site**: http://localhost:3002
   - **Upload Widget**: Built and served from CDN endpoint
   - **Proxy Service**: http://localhost:3003

### Individual Service Setup

If you prefer to run services individually:

```bash
# Backend API
cd apps/nest-backend
npm install
npm run dev

# Frontend Dashboard  
cd apps/frontend
npm install
npm run dev

# Landing Site with Documentation
cd apps/landing-site
npm install
npm run dev

# Upload Widget (build for development)
cd apps/imaginary-widget
npm install
npm run build

# Proxy Service
cd apps/proxy
npm install
npm run dev
```

## 📚 Documentation

Comprehensive documentation is available at the landing site:

- **Widget Documentation**: http://localhost:3002/docs/upload-widget/overview
- **API Documentation**: Available in the backend (`apps/nest-backend/README.md`)
- **Frontend Guide**: Available in the frontend (`apps/frontend/README.md`)

### Key Documentation Sections

- **[Quick Start Guide](apps/landing-site/src/app/docs/upload-widget/quick-start/page.mdx)** - Get up and running in 5 minutes
- **[Installation Options](apps/landing-site/src/app/docs/upload-widget/installation/page.mdx)** - CDN, npm, and self-hosted setup
- **[API Reference](apps/landing-site/src/app/docs/upload-widget/api-reference/page.mdx)** - Complete widget API documentation
- **[Examples](apps/landing-site/src/app/docs/upload-widget/examples/page.mdx)** - Real-world integration examples
- **[Security Guide](apps/landing-site/src/app/docs/upload-widget/security/page.mdx)** - Security best practices

## 🔧 Development

### Available Scripts

From the root directory:

```bash
npm run dev          # Start all services in development mode
npm run build        # Build all applications for production
npm run test         # Run tests across all applications
npm run lint         # Lint all applications
npm run clean        # Clean all build artifacts
```

### Service-Specific Commands

Each application has its own development commands:

```bash
# Widget Development
cd apps/imaginary-widget
npm run dev          # Build with file watching
npm run serve        # Serve built files locally

# Backend Development  
cd apps/nest-backend
npm run dev          # Start with hot reload
npm run test         # Run unit tests
npm run test:e2e     # Run integration tests

# Frontend Development
cd apps/frontend  
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
```

### Development Workflow

1. **Start all services**: `npm run dev` from root
2. **Access applications**:
   - Frontend Dashboard: http://localhost:3000
   - API Documentation: http://localhost:3001/api
   - Landing Site: http://localhost:3002
   - Widget Testing: http://localhost:3002/docs/upload-widget/examples

3. **Make changes**: All services support hot reload
4. **Test integrations**: Use the widget examples to test end-to-end functionality

## 🏗️ Architecture

### System Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Landing Site  │    │  Upload Widget  │
│   Dashboard     │    │  Documentation  │    │  (Embeddable)   │
│                 │    │                 │    │                 │
└─────────┬───────┘    └─────────┬───────┘    └─────────┬───────┘
          │                      │                      │
          └──────────────────────┼──────────────────────┘
                                 │
                    ┌─────────────────┐
                    │   NestJS API    │
                    │    Backend      │
                    │                 │
                    └─────────┬───────┘
                              │
          ┌───────────────────────────────────────┐
          │                                       │
┌─────────▼───────┐                     ┌─────────▼───────┐
│   MongoDB       │                     │  Storage Proxy  │
│   Database      │                     │    Service      │
└─────────────────┘                     └─────────┬───────┘
                                                  │
                                        ┌─────────▼───────┐
                                        │  Cloud Storage  │
                                        │  (AWS S3, GCS)  │
                                        └─────────────────┘
```

### Technology Stack

- **Frontend**: React 18, TypeScript, Vite, Tailwind CSS
- **Backend**: NestJS, TypeScript, MongoDB, Redis
- **Widget**: Vanilla JavaScript, Rollup
- **Landing**: Next.js 14, MDX, Tailwind CSS
- **Proxy**: Node.js, Express, TypeScript
- **Deployment**: Docker, Nginx, Docker Compose

## 🔐 Security Features

- **JWT Authentication** - Secure user authentication and session management
- **API Key Management** - Secure widget authentication with public/private key pairs
- **File Validation** - Comprehensive file type, size, and content validation
- **Access Control** - Fine-grained permissions and file access controls
- **Secure Upload Tokens** - Temporary, signed tokens for secure file uploads
- **CORS Protection** - Proper cross-origin resource sharing configuration

## 🚀 Deployment

### Docker Deployment

```bash
# Production deployment
docker-compose -f deploy/docker-compose.yml up -d

# Local development with Docker
docker-compose -f deploy/docker-compose.local.yml up -d
```

### Manual Deployment

1. **Build all applications**:
   ```bash
   npm run build
   ```

2. **Deploy backend**:
   ```bash
   cd apps/nest-backend
   npm run build
   npm run start:prod
   ```

3. **Deploy frontend**:
   ```bash
   cd apps/frontend
   npm run build
   # Deploy dist/ folder to your CDN
   ```

4. **Deploy widget**:
   ```bash
   cd apps/imaginary-widget
   npm run build
   # Deploy dist/ folder to your CDN
   ```

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines for details.

### Development Setup

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes
4. Run tests: `npm test`
5. Commit your changes: `git commit -m 'Add amazing feature'`
6. Push to the branch: `git push origin feature/amazing-feature`
7. Open a Pull Request

### Code Style

- TypeScript for all new code
- ESLint and Prettier for code formatting
- Conventional commits for commit messages
- Comprehensive tests for new features

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Documentation**: Visit http://localhost:3002/docs/upload-widget/overview
- **Issues**: Create an issue on GitHub
- **Discussions**: Use GitHub Discussions for questions and ideas

## 🙏 Acknowledgments

- Built with amazing open-source technologies
- Inspired by modern file storage needs
- Community-driven development

---

**Ready to build amazing file upload experiences?** 🚀

Start with `npm run dev` and visit the documentation at http://localhost:3002/docs/upload-widget/overview
