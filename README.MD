### Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

Your application will be available at http://localhost:9000.

# Deploying to Vercel

This project uses the community-maintained `vercel-php` runtime. Vercel sends
requests to `api/index.php`, which loads the application entrypoint at
`app/index.php`. The existing Docker setup remains available for local
development and other hosting providers.

## Deploy

1. Import this project into Vercel, or install the Vercel CLI and log in:

   ```sh
   npm install --global vercel
   vercel login
   ```

2. From the project root, run `vercel` and follow the prompts. Use
   `vercel --prod` to deploy to production.

The PHP runtime is configured in `vercel.json`. Add application routes and
content to `app/index.php`. Configure any required secrets in the Vercel
project's environment-variable settings; do not commit them to the repository.
