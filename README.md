# RepoLens Sales Portal

Sales and marketing website for **RepoLens** — Manifest-First Code Review for GitHub.

**Live URL:** [https://sales.repolens.acidni.net](https://sales.repolens.acidni.net)

## Tech Stack

- **Framework:** [Astro](https://astro.build/) 4.x (static output)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) 3.4
- **Hosting:** Azure Static Web Apps
- **CI/CD:** GitHub Actions

## Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview
```

## Deployment

Pushes to `main` automatically deploy via GitHub Actions to Azure Static Web Apps.

### First-Time Setup

1. Create Azure Static Web App in Azure Portal
2. Copy the deployment token
3. Add `AZURE_STATIC_WEB_APPS_API_TOKEN` secret to this GitHub repo
4. Push to `main`

## DNS

| Record | Type | Target |
|--------|------|--------|
| `sales.repolens` | CNAME | Azure SWA hostname |
| `asuid.sales.repolens` | TXT | Azure verification token |

Managed via `acidni-dns` CLI.

## Related

- [RepoLens App](https://repolens.acidni.net)
- [RepoLens Backend Repo](https://github.com/Acidni-LLC/repolens)
- [Product CMDB](https://github.com/Acidni-LLC/acidni-config/tree/main/products/repolens)
