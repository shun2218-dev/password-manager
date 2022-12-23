This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).\

This project uses [Next.js 13](https://nextjs.org/blog/next-13) and adopts app directory structure powered by [`Turbopack`](https://turbo.build/repo).

Only basic authentication is implemented in this application.

## Getting Started

First, run the development server:

```diff_bash
- npm run dev
+ npx turbo dev
# or
- yarn dev
+ yarn turbo dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying ~~`pages/index.tsx`~~ `app/page.tsx`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/auth](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/auth.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## For the part related to Basic Authentication

The authentication decision for Basic Authentication is written in `middleware.ts`.

`pages/api/auth.ts` contains settings for Basic Authentication.

`lib/buffer.ts` contains a function (decodeBase64) to decode the value entered during Basic Authentication from binary data to ASCII. Although not used, a function (endodeBase64) to encode is also provided.

To use Basic Authentication, create an `.env` file and set the user name in `NEXT_PUBLIC_USER` and the password in `NEXT_PUBLIC_PASS` with any value.

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
