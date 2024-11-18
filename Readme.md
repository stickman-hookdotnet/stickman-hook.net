> stickman-hook.net storage base on sanity cms. This article is intended to introduce how to use Sanity.
# Website Project with Sanity CMS


## Overview
This project is a modern web application built with Sanity as the headless CMS. It features a dynamic content management system allowing for easy content updates and maintenance.

## Prerequisites
- Node.js (v14.0.0 or later)
- npm or yarn
- Sanity CLI (`npm install -g @sanity/cli`)

## Tech Stack
- Frontend: Next.js
- CMS: Sanity
- Styling: Tailwind CSS
- Deployment: Vercel (recommended)

## Getting Started

### Installation

1. Clone the repository:
```bash
git clone <your-repository-url>
cd <project-name>
```

2. Install dependencies:
```bash
# Install frontend dependencies
cd web
npm install

# Install Sanity Studio dependencies
cd ../studio
npm install
```

3. Set up environment variables:
```bash
# In /web/.env.local
NEXT_PUBLIC_SANITY_PROJECT_ID=your_project_id
NEXT_PUBLIC_SANITY_DATASET=production
SANITY_API_TOKEN=your_api_token
```

### Development

1. Start the frontend development server:
```bash
cd web
npm run dev
```

2. Start Sanity Studio:
```bash
cd studio
npm run dev
```

## Sanity Studio Configuration

The Sanity Studio is configured in the `/studio` directory. Key configuration files include:

- `sanity.config.ts`: Main configuration file
- `schemas/`: Directory containing all content type definitions
- `desk/`: Custom desk structure configurations

### Content Models

The following content types are defined in the schema:

- Pages
- Navigation
- Settings
- Assets
- SEO configurations

## Deployment

### Frontend Deployment

1. Configure your Vercel project
2. Connect your repository
3. Set environment variables
4. Deploy:
```bash
vercel --prod
```

### Sanity Studio Deployment

Deploy Sanity Studio using:
```bash
cd studio
sanity deploy
```

## Project Structure
```
├── web/                # Frontend application
│   ├── components/     # React components
│   ├── pages/         # Next.js pages
│   ├── lib/           # Utility functions
│   └── public/        # Static assets
│
├── studio/            # Sanity Studio
│   ├── schemas/       # Content models
│   ├── desk/         # Desk configuration
│   └── plugins/      # Custom plugins
```

## Content Management

### Adding New Content Types

1. Create a new schema in `studio/schemas/`
2. Register the schema in `schema.ts`
3. Update the desk structure if needed

### Managing Content

1. Access Sanity Studio at `http://localhost:3333` (development)
2. Use the Studio interface to create and edit content
3. Content changes are reflected in real-time

## Contributing

1. Create a feature branch
2. Make your changes
3. Submit a pull request

## License
MIT

## Support
For support, please raise an issue in the repository or contact the development team.

---

Remember to replace placeholder values (`<your-repository-url>`, `<project-name>`, etc.) with your actual project details.
