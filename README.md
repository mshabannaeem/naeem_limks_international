# Naeem Links International Website

A modern business website built with React, Vite, Tailwind CSS, and an Express contact API. The project includes a marketing homepage, service sections, testimonials, contact form, and a reusable content/data structure for easy updates.

## Overview

This repository contains the full website experience for a digital agency / business brand, including:

- Responsive landing page
- Services overview
- Business value section
- Testimonial section
- Contact form with backend submission handling
- Tailwind-based design system
- Blogger theme export for a separate static blog layout

## Tech Stack

- React 18
- Vite
- Tailwind CSS
- Express.js
- Node.js
- PostCSS

## Project Structure

```bash
.
├── blogger-template.xml
├── index.html
├── package.json
├── postcss.config.js
├── README.md
├── tailwind.config.js
├── vite.config.js
├── name_cover_&_logo/
├── server/
│   ├── app.js
│   ├── index.js
│   └── contact.test.js
├── src/
│   ├── App.jsx
│   ├── data.js
│   ├── index.css
│   ├── main.jsx
│   ├── nli.css
│   └── NLIApp.jsx
└── public/ (if added for images/assets)
```

## Features

- Fast frontend powered by Vite
- Responsive marketing layout
- Contact form posting to a local Express API
- Content stored in a central `src/data.js` file for easy updates
- Easy deployment to static hosting or a hosting platform with Node support
- Blogger template included for website theme export/import workflow

## Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Run the app in development mode

This starts both the backend API and the frontend development server:

```bash
npm run dev
```

- Frontend: http://localhost:5173
- Backend: http://localhost:3001

### 3. Build for production

```bash
npm run build
```

### 4. Preview production build

```bash
npm run preview
```

### 5. Start the production backend

```bash
npm run start
```

## Available Scripts

```bash
npm run dev           # Runs frontend + backend together
npm run dev:client    # Runs the Vite frontend only
npm run dev:server    # Runs the Express server only
npm run build         # Builds the production frontend bundle
npm run preview       # Serves the built app locally
npm run start         # Starts the Express backend
```

## Contact Form Behavior

The contact form submits to the Express backend at:

```http
POST http://localhost:3001/api/contact
```

The API validates the required fields:

- name
- email
- message

If those are provided, it returns a success response. This is suitable for local testing and can later be connected to a real email provider, CRM, or database service for production use.

## Editing Website Content

Most website text and configuration are controlled in `src/data.js`.

You can update:

- services
- testimonials
- stats
- team information
- business details

Example:

```js
export const services = [
  { title: 'Web Designing', category: 'Digital experience', ... },
  { title: 'Web Development', category: 'Web engineering', ... }
];
```

## Blogger Theme

The repository also includes `blogger-template.xml`, which is intended for use in Blogger.

To use it:

1. Open Blogger
2. Go to Theme
3. Select Restore
4. Upload `blogger-template.xml`

This theme is separate from the React app and is intended for the blog/portal version of the site.

## Notes

- The frontend and backend run separately during development.
- The project is configured for local development and demonstration use.
- For production, connect the contact form to a real email or form-processing service.
- Static assets, logos, and images can be added under the project structure as needed.

## License

This project is intended for the website owner and team. If you plan to publish it publicly, confirm the licensing status of all images, branding, and assets before release.

## Contributing

This repository is designed for easy maintenance and content updates. For future changes:

- update site content in `src/data.js`
- add media assets as needed
- rebuild and test before deployment

## Support

For questions or business-related updates, coordinate with the website owner or project maintainer to manage deployment and production content changes.
