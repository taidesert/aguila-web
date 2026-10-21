# Clickable website previews

Use Netlify Deploy Previews so a reviewer can open the actual website in a browser without downloading files or visiting GitHub. Netlify hosts a separate review copy; Hostinger and production DNS are unchanged.

## One-time setup by the account owner

1. Sign in at https://app.netlify.com/ and choose **Add new project** (or **Add new site**), then **Import an existing project**.
2. Choose GitHub. Authorize the Netlify GitHub app for **only** `taidesert/aguila-web`, then select that repository. Do not grant access to unrelated repositories.
3. Choose `main` as the production branch. Choose no framework; leave the base directory, package directory (if shown), and build command empty. Set the publish directory to `.`. No environment variables, secrets, dependencies, or build tools are required.
4. Deploy the project. Its generated `*.netlify.app` address is a review/staging copy of `main`, not the company's production website. Do not connect a custom domain or change DNS.
5. In the project configuration, under **Build & deploy**, verify **Deploy Previews** are enabled for pull requests. Branch deploys are optional and unnecessary. If the plan or account requires approval of an untrusted contributor's preview build, the owner must approve it.
6. After the setup pull request is open, Netlify should build a Deploy Preview for it. If the repository was connected after the pull request was opened, use the Netlify dashboard to trigger/retry its deploy or ask Codex to push a small follow-up change. Do not merge merely to get a preview.
7. Return the generated Netlify project address to Codex. Ask it to check the preview on desktop and mobile and report the direct Deploy Preview link. Setup is complete only once a real PR preview has loaded successfully.

The current account owner may be shown different menu names as Netlify updates its interface. Keep the essential settings above. Check the plan's current deployment limits and access-control options before confirming any paid plan; this setup does not require buying a domain or modifying Hostinger.

## Every future edit

Tell Codex, for example:

> Update the service descriptions. Make a feature branch and a pull request, wait for its Netlify Deploy Preview, and give me the clickable preview URL. Do not merge or publish to Hostinger.

Codex checks the PR's Netlify deployment status, opens and tests the actual URL, and returns it in chat. Reviewers open that link on a desktop or phone; GitHub and screenshots are not necessary for visual review. Unmerged changes stay separate from the review copy of `main` and from Hostinger production. The owner still reviews and merges pull requests.

Preview addresses usually look like `https://deploy-preview-<PR number>--<project name>.netlify.app`; use the URL reported by Netlify rather than guessing one. Updates to the same PR refresh its preview after a successful deploy. Check that the reported deployment corresponds to the latest commit before claiming it is ready.

## Access and privacy

Treat review links as public unless access protection has been explicitly configured and verified. The current site contains only public marketing content and clearly marked contact placeholders. Never put credentials, private customer details, or sensitive draft content into repository files or previews. Any non-site files in the publish directory must also be safe to expose; the current root includes project documentation and static screenshots.

The repository's `netlify.toml` records the publish directory. GitHub app authorization and automatic Deploy Preview activation live in Netlify, not in that file. Adding the file alone does not connect or deploy the project.
