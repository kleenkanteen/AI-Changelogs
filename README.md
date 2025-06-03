# AI Changelogs

## Quickstart

This project uses the [better auth starter](https://github.com/daveyplate/better-auth-nextjs-starter#).

First, create a PostgreSQL db, in supabase ideally, then configure `.env` like this:

```bash
BETTER_AUTH_SECRET=""
DATABASE_URL=""
```

Now generate your schema and perform migrations with drizzle-kit.

```bash
npx @better-auth/cli generate
npx drizzle-kit generate
npx drizzle-kit migrate
```

Now run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) to see the app.

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.