===============================================================================

      ___  ____ ____ ____ ____          ____ ____ ____ _  _ ___
        /  |    |  | |__/ |___          | __ |__/ |  | |  | |__]
       /__ |___ |__| |  \ |___          |__] |  \ |__| |__| |

            ___  _    ____ ____ ___  _ _  _ ____          ____ ___  ____ ____
            |__] |    |___ |___ |  \ | |\ | | __          |___ |  \ | __ |___
            |__] |___ |___ |___ |__/ | | \| |__]          |___ |__/ |__] |___

                                    ____ ____ ____ ___ _ _ _ ____ ____ ____
                                    [__  |  | |___  |  | | | |__| |__/ |___
                                    ___] |__| |     |  |_|_| |  | |  \ |___

===============================================================================
### © 2023 [zCore Group](https://zcoregroup.com)

### zCore Group Website Repository
This repo contains the source code for the zCore Group website for the migration from v1 to v2.
### Description
This is the source code for the zCore Group website. It is a static website built with [Jekyll](https://jekyllrb.com/). The website is hosted on [GitHub Pages](https://pages.github.com/) until the migration to the legacy host GoDaddy is complete.
### Table of Contents
1. Understanding Jekyll
2. Directory Structure
    - 2.1 _about
    - 2.2 _action
    - 2.3 _careers
    - 2.4 _contact
    - 2.5 _counter
    - 2.6 _data
    - 2.7 _delivery
    - 2.8 _includes
    - 2.9 _layouts
    - 2.10 _posts
    - 2.11 _services
    - 2.12 _site
    - 2.13 _team
3. YAML files
    - 3.1 _config.yml
    - 3.2 navigation.yml
4. Workflows
    - 4.1 GitHub Actions
        - 4.1.1 CI.yml
        - 4.1.2 jekyll.yml
        - 4.1.3 dependabot.yml

==========================================================================
1. Understanding Jekyll
Jekyll is a static site generator. It takes text written in your favorite markup language and uses layouts to create a static website. You can tweak how you want the site URLs to look, what data gets displayed on the site, and more.
To add a new page to the site, all you need to do is create a markdown file in the root directory. For example, to create a new page at https://zcoregroup.com/about, create a file named about.md and add the following content:
`---
layout: page
title: About
permalink: /about
---`
This will create a page that uses the layout found in _layouts/page.html and sets the title of the page to About. The permalink is the URL of the page. The page will be accessible at https://zcoregroup.com/about.

2. Directory Structure
- 2.1 _about - Contains the about page content (about-us.md, years-experience.md).
- 2.2 _action - Contains the action page content (call-to-action.md).
- 2.3 _careers - Contains the careers page content (open-position-1 -- open-position-6.md). These files are used to generate the open positions on the careers page.
- 2.4 _contact - Contains the contact page content (phone.md, email.md, offices.md, contact-us.md). These files are used to generate the contact cards on the contact page.
- 2.5 _counter - Contains the counter page content (cups-of-coffee.md, etc.). These files were from the template and serve text into the counter animation that is handled by the counter.js script.
- 2.6 _data - Contains the navigation.yml file (). This file is used to generate the navigation bar on the website.
- 2.7 _delivery - Contains the delivery page content (deliver-innovation.md, deliver-insights.md. deliver-results.md). These files are used to generate the delivery cards on the About page. These were also from the template but were modified to fit the zCore Group brand.
- 2.8 _includes - Contains the header.html, footer.html, and navigation.html files. These files are used to generate the header, footer, and navigation bar on the website.
- 2.9 _layouts - Contains the default.html, page.html, and post.html files. These files are used to generate the default, page, and post layouts on the website. All html files that are generated by Jekyll use one of these files in this directory as a template.
- 2.10 _posts - Contains the blog posts (numerous). These files are used to generate the blog posts on the Insights page.
- 2.11 _services - Contains the services page content (software-development.md, devops.md, data-analytics.md, technology-innovation.md, professional-services.md, transformation.md). These files are used to generate the service cards on the services page.
- 2.12 _site - Contains the generated website files. These files are generated by Jekyll and are not to be edited!!
- 2.13 _team - Contains the team page content (files TBD - wip). These files are used to generate the team cards on the team page.

3. YAML files
- 3.1 _config.yml - Contains the configuration for the Jekyll site. This file is used to set the site title, description, baseurl, theme, etc.
- 3.2 navigation.yml - Contains the navigation bar links. This file is used to generate the navigation bar on the website.

4. Workflows
- 4.1 GitHub Actions
    - 4.1.1 CI.yml - This workflow is used to run the Jekyll build command and deploy the website to GitHub Pages.
    - 4.1.2 jekyll.yml - This workflow is used to run the Jekyll build command and deploy the website to GitHub Pages.
    - 4.1.3 dependabot.yml - This workflow is used to update the dependencies in the Gemfile.lock file.

5. Building Locally
- 5.1 Install Ruby on your machine (https://www.ruby-lang.org/en/documentation/installation/)
- 5.2 Install Jekyll and Bundler (https://jekyllrb.com/docs/installation/)
- 5.3 Run the project locally
  - In the root directory of the project, run the following command to install the dependencies:
    - `bundle install`
  - To build the website, run the following command:
    - `bundle exec jekyll build`
  - To serve the website locally, run the following command:
    - `bundle exec jekyll serve`

===============================================================================
### Roadmap
- [x] Migrate to from v1 to Jekyll v2
- [ ] Migrate from GitHub Pages to GoDaddy
- [ ] Backend integration for database and contact form / CRM / Newsletter
- [ ] Add blog post - Newsletter integration that automates the newsletter as an event-driven workflow
- [ ] Automate everything else
===============================================================================
### [Kanban](https://github.com/orgs/zCoreGroup/projects/1/views/2)

### Google Analytics
- [ ] Add Google Analytics to the website's HTML pages
  - HTML pages are located in the _includes/ directory
- [ ] Add Google Tag Manager to the website
- [ ] Add Google Optimize to the website

Uncomment out and add this tag to the HTML pages on the website that you want to track:

<!-- Google tag (gtag.js) -->
<!-- <script async src="https://www.googletagmanager.com/gtag/js?id=G-JNX8SMN6KY"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-JNX8SMN6KY');
</script> -->

### © 2025 [zCore Group](https://zcoregroup.com)
