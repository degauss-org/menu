# menu

[DeGAUSS Menu](https://degauss.org/menu) is a web application that helps [DeGAUSS](https://degauss.org) users choose [DeGAUSS images](https://degauss.org/available_images). 
This repository contains code for deploying the DeGAUSS menu app in {dht} R package to shinyapps.io and makes it available at [https://degauss.org/menu](https://degauss.org/menu).




## DNS and URL notes

- add a custom URL in the shinyapps.io Dashboard for the application using the "app" subdomain; for example, `http://app.degauss.org/menu`
  - this will require adding a simple, CNAME DNS record for the domain with a record name of `app` (or `app.degauss.org`) and a value of `grapph.shinyapps.io`  (this step is not necessary for `app.degauss.org` and `app.geomarker.io` because they have already been set up
- create an `index.html` file that will serve as a redirect from the github pages site (e.g., `https://degauss.org/menu`, which is based on the name of the github repository *or* can be changed in the repository's Pages settings)
  - this might also require some separate setup to add DNS records such that your URL is directed towards GitHub's servers (but is already done for `degauss.org` and `geomarker.io`)
- in the repository's settings, Pages section, make sure that pages are turned on and directed to serve the correct branch (usually `main`) and folder (usually `/(root)`, so that it will pick up the index.html file to instantly redirect)
