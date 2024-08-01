---
tags: en
dg-publish: true
---

# Overview

|           Static Site Generator            | Rating | Hover previews | Graph view       | Stacked pages | Backlinks        | Password protection | Mobile-friendly | Analytics | Accessible |
|:------------------------------------------:|:------:|:--------------:| ---------------- | ------------- | ---------------- | ------------------- | --------------- | --------- | ---------- |
| [Digital Garden](https://dg-docs.ole.dev/) | 3.5/5  |       ✅       | ✅               | ❌            | ✅               | ❌                  | ✅              | ❌        | ✅         |
|                 quartz ⭐                  |  4/5   |       ✅       | ✅               | ❌            | ✅               | ❌                  | ✅              | ✅        | ✅         |
|   [Flowershow](https://flowershow.app/)    |  3/5   |       ❌       | ❌               | ❌            | ❌               | ❌                  | ✅              | ✅        | ✅         |
|                   MkDocs                   | 2.5/5  |       ❌       | 3rd-Party Plugin | ❌            | 3rd-Party Plugin | ❌                  | ✅              | ✅        | ✅         |


# Obsidian Digital Garden

> [!warning] Requirements
> Assuming you already have:
> - Installed [Digital Garden Plugin](obsidian://show-plugin?id=digitalgarden) in Obsidian.
> - A [GitHub](https://github.com/signup) account.
> - A [Vercel](https://vercel.com/signup) or [Netlify](https://app.netlify.com/signup) account.

The initial setup takes a couple of minutes, but when you're done you'll have a digital garden in which you are in control of every part of it, and can customize it as you see fit. Which is what makes digital gardens so delightful.

## 1. Hosting Platform

### 1.1. Vercel

1. Open [this repo](https://github.com/oleeskild/digitalgarden), and click the blue “Deploy to Vercel” button. 
2. This should open Vercel and create a copy of this repository in your GitHub account.
3. Give it a fitting name like 'my-digital-garden'.
4. Follow the steps in Vercel to publish your site to the internet.
### 1.2. Netlify

1. Open [this repo](https://github.com/oleeskild/digitalgarden) and either clone it or fork it.
2. Go to Netlify and import this repository of your GitHub account.
3. Give it a fitting name like 'my-digital-garden'.
4. Follow the steps in Netlify to publish your site to the internet.

## 2. GitHub Token Generation

> [!tip] A more secure option  
> GitHub has launched a new feature called “Fined-Grained Access Token”, where you can target what repositories the token has access to. This is currently the most secure way to use the plugin.

### 2.1. PAT
1. Next you need to [create a PAT](https://github.com/settings/tokens/new?scopes=repo) to your GitHub Account.
2. The correct settings should already be applied. [^1]
3. Click the “Generate token” button, and copy the token you are presented with on the next page.

[^1]: If you don't want to generate this every few months, choose the “No expiration” option.
### 2.2. FGAT
1. It's a bit more hassle, but you can now create an access token that only have access to the digital garden repo. This is the recommended way to generate your token if you have more repos on your accounts.
2. Remember to regenerate it after the expiration date, as it will no longer work after that date has passed.
3. [Generate it](https://github.com/settings/personal-access-tokens/new), and apply settings as illustrated in the image below:
![[BfxGAQpDcz-700.webp]]

## 3. Plugin Configuration
1. Open Obsidian and the settings for “Digital Garden”.
2. Fill in your GitHub username, the name of the repo with your notes which you created in the 2nd section.
3. Lastly paste in your token.

## 4. Publish your first note!
1. Create a new note in Obsidian.
2. Now add two new properties to the note:
	- A checkbox named `dg-publish`[^2]
	- A checkbox named `dg-home`[^3]
3. Toggle both checkboxes so that they are in the `checked` state if you view as “Live Preview”, or set both as `true`.  
It should look something like this:
![[5CAROmZpll-700.webp]]

[^2]: It tells the plugin that this should be your home page or entry into your digital garden. (It only needs to be added to _one_ note, not every note you'll publish).
[^3]: It tells the plugin that this note should be published to your digital garden. Notes without this setting will not be published. (In other terms: Every note you publish will need this property.)

4. Open the command palette by pressing `CTRL+P` on Windows/Linux or `CMD+P` on Mac.
5. Find the “Digital Garden: Publish Single Note” command and press enter.
6. Go to your site's URL. If nothing shows up yet, wait a minute and refresh. Your note should now appear.

## Done

Congratulations, you now have your own personal part of the internet in the form of a digital garden, for free 🎉.

You can now start adding links as you usually would in Obsidian, with double square brackets, to the note that you just published.

Remember to also publish the notes you are linking to as this will not happen automatically. This is by design. You are always in control of what notes you actually want to publish. If you did not publish a linked note, the link will simply lead to a site telling the user that this note does not exist.

If you want to unpublish a note, without deleting the note from your vault, simply uncheck or remove the `dg-publish` property in the note, open the [publication centre](https://dg-docs.ole.dev/getting-started/02-commands/#open-publication-center) and click the “Delete notes from garden” button.

# Quartz
> [!warning] Requirements
> Assuming you already have:
> - Installed [Enveloppe](obsidian://show-plugin?id=obsidian-mkdocs-publisher) in Obsidian.
> - A Git Account, preferred choice as [GitHub](https://github.com/signup).
> - A [Cloudflare](https://dash.cloudflare.com/sign-up/workers-and-pages), [Vercel](https://vercel.com/signup) or [Netlify](https://app.netlify.com/signup) account (Optional).

## 1.🪴Get Started
Quartz requires **at least [Node](https://nodejs.org/) v18.14** and `npm` v9.3.1 to function correctly. Ensure you have this installed on your machine before continuing.

Then, in your terminal of choice, enter the following commands line by line:
```
git clone https://github.com/jackyzha0/quartz.git
cd quartz
npm i
npx quartz create
```

> [!tip]-
> 
> If you prefer not to install Node in your device, you can skip the steps above and fork it at GitHub. The fork version handles every update from the main directly.

This will guide you through initializing your Quartz with content.

## 2. Writing content

All the content in your Quartz should go in the `/content` folder. The content for the home page of your Quartz lives in `content/index.md`. If you’ve setup Quartz already, this folder should already be initialized. Any Markdown in this folder will get processed by Quartz.

> [!tip]
> It is highly recommended that you use [Obsidian](https://obsidian.md/) as a way to edit and maintain your Quartz. It comes with a nice editor and graphical interface to preview, edit, and link your local files and attachments.

## 3. Setting up your Git repository
1. Create a new repository on GitHub.com, if you haven't.
2. Do not initialize the new repository with README, licence, or `.gitignore` files.

![[Pasted image 20240730100705.png]]

3. At the top of your repository on GitHub.com’s Quick Setup page, click the clipboard to copy the remote repository URL.

![[Pasted image 20240730100738.png]]

4. In your terminal of choice, navigate to the root of your Quartz folder.
5. Then, run the following commands, replacing `REMOTE-URL` with the URL you just copied from the previous step.

```git
# list all the repositories that are tracked
git remote -v

# if the origin doesn't match your own repository, set your repository as the origin
git remote set-url origin REMOTE-URL

# if you don't have upstream as a remote, add it so updates work
git remote add upstream https://github.com/jackyzha0/quartz.git
```

Then, you can sync the content to upload it to your repository. This is a helper command that will do the initial push of your content to your repository.
```
npx quartz sync --no-pull
```


> [!warning]- `fatal: --[no-]autostash option is only valid with --rebase`
> You may have an outdated version of `git`. Updating `git` should fix this issue.

In future updates, you can simply run `npx quartz sync` every time you want to push updates to your repository.

> [!tip] Flags and options
> 
> For full help options, you can run `npx quartz sync --help`.
> 
> Most of these have sensible defaults, but you can override them if you have a custom setup:
> 
> - `-d` or `--directory`: the content folder. This is normally just `content`
> - `-v` or `--verbose`: print out extra logging information
> - `--commit` or `--no-commit`: whether to make a `git` commit for your changes
> - `--push` or `--no-push`: whether to push updates to your GitHub fork of Quartz
> - `--pull` or `--no-pull`: whether to try to pull in any updates from your GitHub fork (i.e. from other devices) before pushing.

## 4. Enveloppe Settings

The root folder must be set as `content` in “File paths”.

## 5. Hosting
Quartz effectively turns your Markdown files and other resources into a bundle of HTML, JS, and CSS files (a website!).

However, if you’d like to publish your site to the world, you need a way to host it online. This guide will detail how to deploy with common hosting providers but any service that allows you to deploy static HTML should work as well.

> [!Warning]
> 
> The rest of this guide assumes that you’ve already created your own GitHub repository for Quartz. If you haven’t already, [make sure you do so.](https://quartz.jzhao.xyz/setting-up-your-GitHub-repository)

> [!Hint]
> 
> Some Quartz features (like [RSS Feed](https://quartz.jzhao.xyz/features/RSS-Feed) and sitemap generation) require `baseUrl` to be configured properly in your [configuration](https://quartz.jzhao.xyz/configuration) to work properly. Make sure you set this before deploying!

### GitHub Pages

In your local Quartz, create a new file `quartz/.github/workflows/deploy.yml`.

```yml
# quartz/.github/workflows/deploy.yml

name: Deploy Quartz site to GitHub Pages
 
on:
  push:
    branches:
      - v4
 
permissions:
  contents: read
  pages: write
  id-token: write
 
concurrency:
  group: "pages"
  cancel-in-progress: false
 
jobs:
  build:
    runs-on: ubuntu-22.04
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0 # Fetch all history for git info
      - uses: actions/setup-node@v4
      - name: Install Dependencies
        run: npm ci
      - name: Build Quartz
        run: npx quartz build
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: public
 
  deploy:
    needs: build
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

Then:

1. Head to “Settings” tab of your forked repository and in the sidebar, click “Pages”. Under “Source”, select “GitHub Actions”.
2. Commit these changes by doing `npx quartz sync`. This should deploy your site to `<github-username>.github.io/<repository-name>`.

> [!Hint]
> 
> If you get an error about not being allowed to deploy to `github-pages` due to environment protection rules, make sure you remove any existing GitHub pages environments.
> 
> You can do this by going to your Settings page on your GitHub fork and going to the Environments tab and pressing the rubbish icon. The GitHub action will recreate the environment for you correctly the next time you sync your Quartz.

> [!Info]
> Quartz generates files in the format of `file.html` instead of `file/index.html` which means the trailing slashes for _non-folder paths_ are dropped. As GitHub pages don't do this redirect, this may cause existing links to your site that use trailing slashes to break. If not breaking existing links is important to you (e.g. you are migrating from Quartz 3), consider using Cloudflare Pages.


#### Custom Domain[](https://quartz.jzhao.xyz/hosting#custom-domain)

Here’s how to add a custom domain to your GitHub pages deployment.

1. Head to the “Settings” tab of your forked repository.
2. In the “Code and automation” section of the sidebar, click “Pages”.
3. Under “Custom Domain”, type your custom domain and click “Save”.
4. This next step depends on whether you are using an apex domain (`example.com`) or a subdomain (`subdomain.example.com`).
    - If you are using an apex domain, navigate to your DNS provider and create an `A` record that points your apex domain to GitHub’s name servers which have the following IP addresses:
        - `185.199.108.153`
        - `185.199.109.153`
        - `185.199.110.153`
        - `185.199.111.153`
    - If you are using a subdomain, navigate to your DNS provider and create a `CNAME` record that points your subdomain to the default domain for your site. For example, if you want to use the subdomain `quartz.example.com` for your user site, create a `CNAME` record that points `quartz.example.com` to `<github-username>.github.io`.

![[Pasted image 20240730103144.png|The above shows a screenshot of Google Domains configured for both `jzhao.xyz` (an apex domain) and `quartz.jzhao.xyz` (a subdomain).]]

See the [GitHub documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain) for more detail about how to set up your own custom domain with GitHub Pages.

> [!warning] Why aren't my changes showing up?
> 
> There could be many reasons why your changes aren’t showing up, but the most likely reason is that you forgot to push your changes to GitHub.
> 
> Make sure you save your changes to Git and sync it to GitHub by doing `npx quartz sync`. This will also make sure to pull any updates you may have made from other devices so you have them locally.

3. [Writing content](https://quartz.jzhao.xyz/authoring-content) in Quartz
4. [Configure](https://quartz.jzhao.xyz/configuration) Quartz’s behaviour
5. Change Quartz’s [layout](https://quartz.jzhao.xyz/layout)
6. [Build and preview](https://quartz.jzhao.xyz/build) Quartz
7. Sync your changes with [GitHub](https://quartz.jzhao.xyz/setting-up-your-GitHub-repository)
8. [Host](https://quartz.jzhao.xyz/hosting) Quartz online

If you prefer instructions in a video format you can try following Nicole van der Hoeven’s [video guide on how to set up Quartz!](https://www.youtube.com/watch?v=6s6DT1yN4dw&t=227s)

### GitLab Pages

In your local Quartz, create a new file `.gitlab-ci.yml`.

```yml
# .gitlab-ci.yml

stages:
  - build
  - deploy
 
image: node:18
cache: # Cache modules in between jobs
  key: $CI_COMMIT_REF_SLUG
  paths:
    - .npm/
 
build:
  stage: build
  rules:
    - if: '$CI_COMMIT_REF_NAME == "v4"'
  before_script:
    - hash -r
    - npm ci --cache .npm --prefer-offline
  script:
    - npx quartz build
  artifacts:
    paths:
      - public
  tags:
    - docker
 
pages:
  stage: deploy
  rules:
    - if: '$CI_COMMIT_REF_NAME == "v4"'
  script:
    - echo "Deploying to GitLab Pages..."
  artifacts:
    paths:
      - public
```

When `.gitlab-ci.yaml` is committed, GitLab will build and deploy the website as a GitLab Page. You can find the URL under `Deploy > Pages` in the sidebar.

By default, the page is private and only visible when logged in to a GitLab account with access to the repository but can be opened in the settings under `Deploy` → `Pages`.

### Cloudflare Pages

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/) and select your account.
2. In Account Home, select **Workers & Pages** > **Create application** > **Pages** > **Connect to Git**.
3. Select the new GitHub repository that you created and, in the **Set up builds and deployments** section, provide the following information:

| Configuration option   | Value              |
| ---------------------- | ------------------ |
| Production branch      | `v4`               |
| Framework preset       | `None`             |
| Build command          | `npx quartz build` |
| Build output directory | `public`           |

Press “Save and deploy” and Cloudflare should have a deployed version of your site in about a minute. Then, every time you sync your Quartz changes to GitHub, your site should be updated.

To add a custom domain, check out [Cloudflare’s documentation](https://developers.cloudflare.com/pages/platform/custom-domains/).

> [!Warning]
> 
> Cloudflare Pages performs a shallow clone by default, so if you rely on `git` for timestamps, it is recommended that you add `git fetch --unshallow &&` to the beginning of the build command (e.g., `git fetch --unshallow && npx quartz build`).

### Vercel

#### Fix URLs

Before deploying to Vercel, a `vercel.json` file is required at the root of the project directory. It needs to contain the following configuration so that URLs don’t require the `.html` extension:

```json
# vercel.json

{
  "cleanUrls": true
}
```

#### Deploy to Vercel

1. Log in to the [Vercel Dashboard](https://vercel.com/dashboard) and click “Add New…” > Project
2. Import the Git repository containing your Quartz project.
3. Give the project a name (lowercase characters and hyphens only)
4. Check that these configuration options are set:

| Configuration option                      | Value              |
| ----------------------------------------- | ------------------ |
| Framework Preset                          | `Other`            |
| Root Directory                            | `./`               |
| Build and Output Settings > Build Command | `npx quartz build` |

5. Press Deploy. Once it’s live, you’ll have 2 `*.vercel.app` URLs to view the page.

#### Custom Domain

> [!Note]
> 
> If there is something already hosted on the domain, these steps will not work without replacing the previous content. As a workaround, you could use Next.js rewrites or use the next section to create a subdomain.

1. Update the `baseUrl` in `quartz.config.js` if necessary.
2. Go to the [Domains  — Dashboard](https://vercel.com/dashboard/domains) page in Vercel.
3. Connect the domain to Vercel
4. Press “Add” to connect a custom domain to Vercel.
5. Select your Quartz repository and press Continue.
6. Enter the domain you want to connect it to.
7. Follow the instructions to update your DNS records until you see “Valid Configuration”

#### Use a Subdomain

Using `docs.example.com` is an example of a subdomain. They’re a simple way of connecting multiple deployments to one domain.

1. Update the `baseUrl` in `quartz.config.js` if necessary.
2. Ensure your domain has been added to the [Domains - Dashboard](https://vercel.com/dashboard/domains) page in Vercel.
3. Go to the [Vercel Dashboard](https://vercel.com/dashboard) and select your Quartz project.
4. Go to the Settings tab and then click Domains in the sidebar
5. Enter your subdomain into the field and press Add

### Netlify

1. Log in to the [Netlify dashboard](https://app.netlify.com/) and click “Add new site”.
2. Select your Git provider and repository containing your Quartz project.
3. Under “Build command”, enter `npx quartz build`.
4. Under “Publish directory”, enter `public`.
5. Press Deploy. Once it’s live, you’ll have a `*.netlify.app` URL to view the page.
6. To add a custom domain, check “Domain management” in the left sidebar, just like with Vercel.

### Self-Hosting

Copy the `public` directory to your web server and configure it to serve the files. You can use any web server to host your site. Since Quartz generates links that do not include the `.html` extension, you need to let your web server know how to deal with it.

#### Using Nginx

Here’s an example of how to do this with Nginx:

```nginx
# nginx.conf

server {
    listen 80;
    server_name example.com;
    root /path/to/quartz/public;
    index index.html;
    error_page 404 /404.html;
 
    location / {
        try_files $uri $uri.html $uri/ =404;
    }
}
```

#### Using Caddy

Here’s an example of how to do this with Caddy:

```
# Caddyfile

example.com {
    root * /path/to/quartz/public
    try_files {path} {path}.html {path}/ =404
    file_server
    encode gzip
 
    handle_errors {
        rewrite * /{err.status_code}.html
        file_server
    }
}

```