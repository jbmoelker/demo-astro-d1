# Demo Astro D1

**Proof-of-concept for a full-stack application using web standard first frameworks, libraries and services.**

## Architecture

The application is created as a full-stack setup including auth, a database, and server-side rendering:

- [Astro](https://astro.build/) - web framework to structure this project. Astro is selected because it embraces web standards, is designed for performance, provides server-side rendering as a baseline and supports all our favourite UI frameworks (React, Vue and Svelte) for future enhancement.
- [Cloudflare D1](https://developers.cloudflare.com/d1/) - edge database based on SQLite web standard. Plays nicely with an ORM like [Drizzle ORM](https://orm.drizzle.team/), which provides a convenient [Studio UI](https://orm.drizzle.team/drizzle-studio/overview) for the database.
- [Cloudflare Pages](https://developers.cloudflare.com/pages/) - hosting with CDN, edge worker support and native integration into D1 database.
- [Auth.js](https://authjs.dev/) - generic auth library with a [Cloudflare D1 adapter](https://authjs.dev/reference/adapter/d1) (and [Drizzle ORM adapter](https://authjs.dev/reference/adapter/drizzle)) and a community developed [Astro integration](https://github.com/nowaythatworked/auth-astro).
