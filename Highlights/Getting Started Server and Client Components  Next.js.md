---
URL: https://nextjs.org/docs/app/getting-started/server-and-client-components
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/ddb7e00cb189c21a705b
Tags: []
Last updated: 2025-10-10
---
#### Highlights & Notes

> To reduce the size of your client JavaScript bundles, add 'use client' to specific interactive components instead of marking large parts of your UI as Client Components.

> props として提供されるものも含め、すべてのサーバーコンポーネントが事前にサーバー上でレンダリングされます。結果として得られる RSC ペイロードには、コンポーネントツリー内でクライアントコンポーネントがレンダリングされる場所への参照が含まれます。

> Your Server Component will now be able to directly render your provider, and all other Client Components throughout your app will be able to consume this context.

> In Next.js, only environment variables prefixed with NEXT_PUBLIC_ are included in the client bundle. If variables are not prefixed, Next.js replaces them with an empty string.


