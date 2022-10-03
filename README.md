Automatic Build of Hugo website using hugo-resume theme with Github Actions Pipeline and Deploy to Github pages..

To create your own free website at "{yourgituser}.github.io":
1. Fork this repo and rename it while being forked
2. Rename the repository to {yourgituser}.github.io
3. IMPORTANT: While at your new repo, Go to Settings > Go to Pages > At "Build and deployment - Source" select "Github Actions" from the dropdown!
4. Do a manual change in one of the files to force a commit and start the pipeline. Just change something in config.toml
5. Go to {yourgituser}.github.io <br><br>
<B>(optional for netlify)</B><br><br>
6. Register and create a new site at Netlify. Edit --baseURL in netlify.toml to match your newly created site in netlify.<br>
7. To refresh pages in GithubPages we need to recompile our theme inside themes/ folder each time we run the pipeline<br> https://github.com/cryptozealot/cryptozealot.github.io/blob/master/.github/workflows/pages.yml#L48
Netlify needs that created in the repo prior to the deploy(maybe there is a fix for this - TODO)
So before we run Netlify Deployment, we clone our repo locally and cd into it, then we run:

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



Original Readme Is Below:
<br>###################################################
<br>###################################################
# hugo Resume

Created from [Start Bootstrap - Resume](https://startbootstrap.com/template-overviews/resume/).
This is basically a single-page website with auto-scrolling based on left-hand nav.  Dedicated project/publications pages allow more detail.  Includes a client-side search powered by fuse.js at '/search' but currently theme does not link to that anywhere.  Includes an `/admin` endpoint that can allow authorized users to use a WYSIWYG editor and commit files back to markdown, but with a Wordpress/CMS like experience.

<!-- MarkdownTOC autolink="true" -->

- [Examples](#examples)]

- [Setup & Use](#setup--use)
    - [Summary](#summary)
    - [Data files](#data-files)
    - [Projects](#projects)
    - [Publications](#publications)
    - [Blog / Posts](#blog--posts)
    - [Template params](#template-params)tgggtgc
- [CMS Editor with Netlify CMS](#cms-editor-with-netlify-cms)
- [Credits](#credits)
    - [Contributions](#contributions)
    - [Start Bootstrap Resume](#start-bootstrap-resume)

<!-- /MarkdownTOC -->

See [Eddie's site](https://edwardawebb.com) for a live example.

## Setup & Use

This theme uses a combination of a custom archetype `projects` and some data files to drive content.

You can test the provided [exampleSite](exampleSite) after cloning with the command:
`cd exampleSite;hugo -t hugo-resume --themesDir ../.. server`

### Summary
Edit the main `contents/_index.md with a brief bio/summary`

### Data files
Data files are used for simple content presented on the homepage.

- [data/skills.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/skills.json)
- [data/experience.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/experience.json)
- [data/education.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/education.json)


### Projects
Initially projects were in their own JSON file too, but I decided I wanted to allow more detail and custom formatting.
Projects are added to one of 2 subfolders of `creations` or `contributions`. The difference indicates your role as originator or colaborator.   Use `hugo add projects/TYPE/name-of-project.md` to leverage the proper archetype.

### Publications
Similar to projects, create them under `publications`. Include any papers, speaking engagements, articles, etc.

### Blog / Posts
Similar to posts, create them under `blog`. Include any thoughts, musiings, etc.
**This template does not support a `posts` folder**

### Template params

All personal information outside the above details is captured by params in [`config.toml`](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/config.toml), or can be edited in the "Settings" collection if using CMS.

## CMS Editor with Netlify CMS
**Does not require deployment to Netlify!**

[Netlify CMS](https://www.netlifycms.org/) is an open source project that enables CMS like experience for static site generation tools like Hugo. This theme includes a fully working integration and guide in [exampleSite/static/admin](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/static/admin)

![CMS integration](/images/cms.png)


## Credits

This project ports the Start Bootstrap Resume theme by David Miller to support hugo.

### Contributions
The following users have made notable contributions:
- [Anthony Whitford](https://github.com/awhitford)
- [Kaushal Modi](https://github.com/kaushalmodi)
- [Julien Rouse](https://github.com/JulienRouse)

### Start Bootstrap Resume

Start Bootstrap is an open source library of free Bootstrap templates and themes. All of the free templates and themes on Start Bootstrap are released under the MIT license, which means you can use them for any purpose, even for commercial projects.

* https://startbootstrap.com
* https://twitter.com/SBootstrap

Start Bootstrap was created by and is maintained by **[David Miller](http://davidmiller.io/)**, Owner of [Blackrock Digital](http://blackrockdigital.io/).

* http://davidmiller.io
* https://twitter.com/davidmillerskt
* https://github.com/davidtmiller

Start Bootstrap is based on the [Bootstrap](http://getbootstrap.com/) framework created by [Mark Otto](https://twitter.com/mdo) and [Jacob Thorton](https://twitter.com/fat).

