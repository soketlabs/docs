# Mintlify Starter Kit

Click on `Use this template` to copy the Mintlify starter kit. The starter kit contains examples including

- Guide pages
- Navigation
- Customizations
- API Reference pages
- Use of popular components

### Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mintlify) to preview the documentation changes locally. This project includes Mintlify as a local dependency, so use the pinned Node version in `.nvmrc`.

```
nvm install 24
nvm use 24
npm install
npm run dev
```

If you prefer a global CLI install, use a supported Node version (Node 24 is recommended):

```
npm i -g mintlify@latest
mintlify dev
```

If you hit a Node 25 compatibility error, downgrade to Node 24 or another active LTS release.

### Publishing Changes

Install our Github App to auto propagate changes from your repo to your deployment. Changes will be deployed to production automatically after pushing to the default branch. Find the link to install on your dashboard. 

#### Troubleshooting

- **Stuck on "preparing local preview..."** — Stop the server (Ctrl+C), then run `npm run dev` again. The first start can take 30–60 seconds while OpenAPI and pages are built. Use Node 24 (`nvm use`). Avoid `npx mintlify dev`; this repo uses the local CLI via `npm run dev`. If you only need prose pages (no API playground), use `npm run dev:quick`.
- Mintlify dev isn't running — Run `npm install`, then `npm run dev`.
- Page loads as a 404 — Run from the repo root that contains `docs.json`.
