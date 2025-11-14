# Full stack AI

Build a full stack Next.js app from an AI prompt.

## What It Does

Full Stack AI, `fsai`, is a CLI that uses AI to build a full-stack app for you.

The AI will:

* Generate a Next.js app with TypeScript and Tailwind
* Add shadcn/ui for frontend components
* Generate pages to create/update/delete data
* Generate a Prisma/Drizzle schema
* Uses Postgres/MySQL/SQLite for the database
* Add auth via NextAuth.js with GitHub/Discord/Google/Apple log in supported
* Or add auth with Clerk/Lucia/Kinde
* Add account screen to change settings
* Add Stripe for payments
* Add Resend to send transactional emails
* Generate CRUD APIs
* Add light/dark mode

It can use the package manager of your choice. It defaults to `pnpm` unless you prompt the AI otherwise.

### Experimentation

We've been experimenting with a more general AI coder called [Aleph0](https://github.com/alephmatic/aleph0) which is in beta.

## Getting Started

```bash
export OPENAI_API_KEY=...
npx fsai gen "Build a clone of Twitter called StackPrompt where people prompt instead of tweet. Allow users to follow one another and to like prompts. Use GitHub for log in. Charge users a monthly fee for premium functionality."
```

Then `cd` into the newly created app folder, set the environment variables and in the `.env` file and run `npm run dev` to see your app live in the browser at [http://localhost:3000](http://localhost:3000).

You can install the package globally and run as follows:

```bash
pnpm i -g fsai
export OPENAI_API_KEY=...
fsai gen "Build a clone of Twitter called StackPrompt where people prompt instead of tweet. Allow users to follow one another and to like prompts. Use GitHub for log in. Charge users a monthly fee for premium functionality."
```

## Run locally

If you want to clone the repo and run it locally:

```bash
pnpm i
export OPENAI_API_KEY=...
npx tsx src/index.ts gen "Build a clone of Twitter called StackPrompt where people prompt instead of tweet. Allow users to follow one another and to like prompts. Use GitHub for log in. Charge users a monthly fee for premium functionality."
```
