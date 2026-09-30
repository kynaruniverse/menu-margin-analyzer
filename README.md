# MenuIQ website

A GitHub/Vercel-ready static site for MenuIQ, including:

- A marketing homepage at `/`.
- The working browser app at `/app/`.
- CSV templates inside `/app/`.
- No build step and no secret keys.

## Run locally

From this folder:

```bash
python3 -m http.server 4173
```

Open <http://localhost:4173>.

## Upload to GitHub

Create an empty repository on GitHub, then run:

```bash
git init
git add .
git commit -m "Prepare MenuIQ website and app"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the remote URL with your own repository URL.

## Deploy with Vercel

### Easiest route

1. Sign in at <https://vercel.com>.
2. Choose **Add New → Project**.
3. Import the GitHub repository.
4. Leave **Framework Preset** as **Other**.
5. Leave the build command empty.
6. Set the output directory to `.` if Vercel asks for one.
7. Deploy.

Every future push to `main` will create a new deployment when the repository is connected.

### CLI route

If you prefer the terminal:

```bash
npm install --global vercel
vercel
```

Run that command from this folder and follow the prompts. Use `vercel --prod` only when you are ready to publish the current version to production.

## Before public sale

- Replace the placeholder licence with final legal terms.
- Replace `hello@menuiq.example` in `index.html` with a real contact address.
- Add your Gumroad checkout URL to the homepage once the product listing exists.
- Add a real privacy policy before collecting email addresses or account data.
- Decide whether the offline app should remain free or be placed behind a purchase link.

The current app stores data locally in the visitor's browser. It is not yet a cloud SaaS and does not provide accounts or synchronisation.
