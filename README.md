# netomat blog (blog.netomat.io)

Hugo site using [PaperMod](https://github.com/adityatelange/hugo-PaperMod) with the
netomat-theme brand layer on top.

## Local development

```bash
git clone --recurse-submodules git@github.com:netomat/blog.git
hugo server -D          # serve with drafts at http://localhost:1313
hugo                    # production build into public/
```

## Writing a post

```bash
hugo new content posts/my-post.md    # starts as draft: true
```

Remove `draft: true` when the post is ready to publish
(preview drafts locally with `hugo server -D`).

## Updating the shared theme

```bash
git submodule update --remote themes/netomat
git add themes/netomat && git commit -m "Bump netomat theme"
```

Never override layouts locally — visual changes belong in the netomat-theme repo.

## Cloudflare Pages settings

- Build command: `hugo --gc --minify`
- Build output directory: `public`
- Environment variable: `HUGO_VERSION = 0.165.0`
