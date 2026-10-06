# Cluster - AI-powered Travel Platform

An interactive travel planning platform with AI personalization, 3D tours, and B2B solutions for businesses.

## 🌟 Key Features

- **🎯 Wow effect**: Interactive 3D tours of attractions (AVALIN)
- **🤖 AI personalization**: Smart recommendations based on preferences
- **💼 B2B value**: Partner dashboard for managing places and special offers
- **🗺️ Smart routes**: Seasonal recommendations and travel optimization
- **🔍 Semantic search**: Search for places in natural language

## 🚀 Quick Start

### Requirements

- Docker Desktop (Windows/Mac) or Docker + Docker Compose (Linux)
- Available ports: 5432, 8000, 5173

### Windows (recommended)

```powershell
.\setup_db.ps1
```

### Linux/macOS

```bash
./server_app/scripts/setup_all.sh
```

## 🌐 Available Services

After launch:

- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs
- **PostgreSQL**: localhost:5432

## 🏗️ Architecture

```
Cluster/
├── client_app/          # Vue 3 + TypeScript frontend
├── server_app/          # FastAPI backend
├── docker-compose.yml   # Docker configuration
└── scripts/            # Setup scripts
```

### Frontend (client_app)

- **Vue 3** with Composition API and `<script setup>`
- **TypeScript** for typing
- **Vite** for fast builds
- **Leaflet** for interactive maps
- **AVALIN Viewer** for 3D tours

### Backend (server_app)

- **FastAPI** with automatic documentation
- **PostgreSQL** with SQLAlchemy ORM
- **Alembic** for migrations
- **Local TF-IDF** for semantic place search (built-in, free)
- **DeepSeek Chat API** for future features (optional)
- **OpenAI/other embeddings** as an alternative (optional)
- **JWT** authentication for partners

## 📊 Demo Data

The project includes 18 demo places with:

- ✅ AVALIN 3D tours
- ✅ Special offers from businesses
- ✅ AI embeddings for semantic search
- ✅ Photos and descriptions
- ✅ Geolocations and prices

## 🔧 Development

### Running in development mode

```bash
# Backend
cd server_app
uvicorn main:app --reload --host 0.0.0.0 --port 8000

# Frontend
cd client_app
npm run dev
```

### API Structure

- `GET /places` - Get all places
- `GET /places/{id}` - Detailed information about a place
- `POST /places/search` - Semantic search
- `POST /route/generate` - Generate route
- `POST /partner/auth/*` - Partner authorization
- `GET /partner/places` - Partner places

### Database

| Parameter | Value |
|----------|----------|
| Host     | localhost |
| Port     | 5432 |
| Database | clusterdb |
| User     | cluster_user |
| Password | password |

Connection string: `postgresql://cluster_user:password@localhost:5432/clusterdb`

## 🎯 For the Hackathon

### Key Advantages

1. **Wow effect**: 3D tours create an impressive user experience
2. **B2B model**: Partners can add places and special offers
3. **AI innovations**: Personalization based on embeddings
4. **Scalability**: Easily add new places and features

### Demo for Judges

1. Launch the project with `.\setup_db.ps1`
2. Open http://localhost:5173
3. Try 3D tours (the "3D tour" buttons on place cards)
4. Generate a personalized route
5. Go to the partner dashboard for a B2B demo

## 📝 License

The project was developed for a hackathon. MIT License.

## 🤝 Contributors

- Cluster Hackathon development team
