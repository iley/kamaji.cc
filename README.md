# Kamaji.cc website source code

Here you'll find source code for the [Kamaji website](https://kamaji.cc).

The site is built with [Hugo](https://gohugo.io).

## Build and deploy

 * `hugo` - build;
 * `hugo serve` - run a local webserver for preview;
 * `hugo deploy` - deploy to S3.

## Update Hugo version

The Hugo version is configured in multiple places:

 * **Local development**: Update Hugo using your package manager (e.g., `brew upgrade hugo`)
 * **GitHub Actions CI**: `.github/workflows/deploy.yaml` - update the `hugo-version` field
 * **Cloudflare Pages**: Set the `HUGO_VERSION` environment variable in your Cloudflare Pages project settings (Settings → Environment variables)

Make sure all environments use the same Hugo version to ensure consistent builds.
