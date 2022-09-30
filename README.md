# `turbo-repro-cookie-file`

This attempts to repro https://github.com/vercel/turborepo/issues/2134

1. Create with `npx create-turbo` (selected name and `npm` as package manager)
2. `npm i -D turbo@1.4` to downgrade turbo
3. `npm run build` (which proxies to `turbo run build`) to see build run successfully
4. `ls .turbo-cookie` to make sure it doesn't get created.
5. `npm i -D turbo@1.5`
6. `npm run build` and then `ls .turbo-cookie` again
