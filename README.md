[![Netlify Status](https://api.netlify.com/api/v1/badges/338b24b5-0c9c-4c7f-9c61-589f40985a94/deploy-status)](https://app.netlify.com/sites/cryptozealot/deploys)<br>
![example workflow](https://github.com/cryptozealot/cryptozealot.github.io/actions/workflows/pages.yml/badge.svg)<br>
[![Website status](https://img.shields.io/website-up-down-green-red/https/laborecke.de.svg?label=Website%20status)](https://cryptozealot.github.io)

# Code base of [cryptozealot.github.io](https://cryptozealot.github.io/)

##### A dynamic staticly generated HTML website using Hugo and Hugo-Resume theme built and deployed with Github Actions Workflows to Github Pages and adminstered with Netlify CMS admin panel.

AKA a free automatically deployed dynamic website hosted on Github without a database.

<b>To create your own free website at "{yourgituser}.github.io":</b>

1. Fork this repo and rename it while being forked
2. Rename the repository to {yourgituser}.github.io
3. IMPORTANT: While at your new repo, Go to Settings > Go to Pages > At "Build and deployment - Source" select "Github Actions" from the dropdown!
4. IMPORTANT: While at your new repo, Go to Settings > Go to Actions > Click Enable Actions
5. Do a manual change in one of the files to force a commit and start the pipeline. Just change something in config.toml
6. Go to {yourgituser}.github.io <br><br>
<B>(optional for netlify)</B><br><br>
6. Register and create a new site at Netlify. Edit --baseURL in netlify.toml to match your newly created site in netlify.<br>

NOTE: If there are issues with the module, clone locally, run cmd below, and push back to remote. 

```git submodule add https://github.com/cryptozealot/cryptozealot.github.io.git /themes/hugo-resume/```

Changes made to original repo:
1. Added .github/workflows/ "Github Actions" workflow to build and deploy on Github Pages.
2. Added netlify.toml - for Netlify deployment and admin panel
3. Created theme file, moved folders from exampleSite, cleanup

Resources:
<br>https://02dev.com/post/learn/61d8edb69c67d2983d96fae8
<br>https://www.netlifycms.org/docs/github-backend/
<br>https://www.netlifycms.org/docs/git-gateway-backend/
<br>https://preview-auth-doc--netlify-cms-www.netlify.app/docs/authentication-backends/#github-backend
<br>https://docs.netlify.com/visitor-access/oauth-provider-tokens/#using-an-authentication-provider
<br>https://docs.netlify.com/visitor-access/oauth-provider-tokens/#netlify-ui-settings
<br>https://cloud.gov/pages/documentation/getting-started-with-netlify-cms/
