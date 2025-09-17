# Lt. Dan's Leaderboard API

A robust REST API for managing high scores and leaderboards for Lt. Dan's Run for Re-Election game.

## Features

- **PostgreSQL Integration**: Persistent score storage
- **Anti-Cheat Measures**: Score validation and rate limiting
- **Security**: Input sanitization, CORS, helmet security headers
- **Performance**: Optimized database queries with indexing
- **Real-time Rankings**: Instant rank calculation on score submission

## API Endpoints

### Core Endpoints
- `GET /api/health` - Health check
- `POST /api/scores` - Submit new score
- `GET /api/leaderboard/global` - Get global leaderboard
- `GET /api/leaderboard/recent` - Get recent scores
- `GET /api/leaderboard/rank/:score` - Get rank for score
- `GET /api/player/:name/best` - Get player stats

## Deployment

This API is designed to be deployed on Railway with PostgreSQL database integration.

### Environment Variables
- `DATABASE_URL`: PostgreSQL connection string
- `NODE_ENV`: Environment (production/development)
- `PORT`: API port (default: 3001)

## Security Features

- Rate limiting (10 submissions per 5 min)
- Input validation and sanitization
- Anti-cheat score validation
- CORS protection
- Security headers via Helmet

---

*Part of Lt. Dan's Run for Re-Election game ecosystem*