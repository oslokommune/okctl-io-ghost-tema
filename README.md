![Logo](.github/assets/img/github-header.png)

# OKCTL.io Ghost.io Theme

Based on the DigiDocs theme from Themeforest and the [custom okctl](https://github.com/oslokommune/okctl-ghost-theme) theme by @DanielElisenberg.

## Repository Configuration
The repository is built and deployed using Github Actions, directly to ghost.io, converting the assets/scss/screen.scss file to CSS using Gulp.


## Local Development
### Requirements
- Node v. 14.9.1 (**Important!** Will not work on Node v. 15 or newer, or v. 14.7 or older.)
- Gulp
- Docker-Compose

### Setup
- Run `npm install`
- Run `gulp` to build the theme
- Modify [docker-compose.yml](docker-compose.yml) to ensure the correct mapping of the volume to `/var/lib/ghost/content/themes/okctl-ghost-theme`
- Run `docker-compose up` to start the development environment
- Access the site at http://localhost:80 or http://localtest.me (redirects to http://127.0.0.1)
- Once on the site, use /ghost to create the site.
- You will need to export the content, route, and redirect files from okctl.io and then import them into the local Ghost site for the theme to work.
    - This is done from the okctl.io Ghost admin panel -> Settings -> Labs
- Modify the local sites setting, and select the "Digidocs" theme from the "Advanced" dropdown at the top.

### Notes:
- Run `docker-compose down` to stop the development environment
- Run `docker-compose restart` to restart the development environment
- Run `docker-compose logs` to see the logs
- Run `docker-compose ps` to see the running containers


To test locally, you'll need [NPM](https://www.npmjs.com/) installed, which allows you to install the gulp CLI globally using:
```bash
npm install gulp-cli -g
```

If you don't have Node installed, download NVM and use it to manage multiple versions of NodeJS on your machine.

## Production
Push the code to a branch and merge to master to automatically build and deploy the theme on okctl.io.
