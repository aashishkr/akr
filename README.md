# aashishkumar.vercel.app

Personal website built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. Deployed on Vercel.

## Stack

- **Framework:** Hugo (static site generator)
- **Theme:** PaperMod
- **Hosting:** Vercel
- **Contact form:** Web3Forms
- **Analytics:** Vercel Analytics

## Local Development

```bash
hugo server
```

Visit `http://localhost:1313`.

## Project Structure

```
content/        # Page content (Markdown)
layouts/        # Template overrides
static/images/  # Static assets
hugo.yaml       # Site configuration
```

## Deployment

Pushes to `master` auto-deploy via Vercel. Build config is in `vercel.json`.
