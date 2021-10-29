# OKCTL.io Ghost.io Theme

Based on the DigiDocs theme from Themeforest and the [custom okctl](https://github.com/oslokommune/okctl-ghost-theme) theme by @DanielElisenberg.

## Repository Configuration
The repository is built and deployed using Github Actions, directly to ghost.io, converting the assets/scss/screen.scss file to CSS using Gulp. 

To test locally, you'll need [NPM](https://www.npmjs.com/) installed, which allows you to install the gulp CLI globally using:
```bash
npm install gulp-cli -g
```

You can then build the code using:

```bash
gulp build
```

To push updates to the theme to production, push the code to main, which in turn will deploy to ghost.io automatically.

## Local Installation
Installing ghost.io locally, allows for updates in real-time. The easiest way to run ghost locally is by deploying the Docker image, available on Docker Hub: https://hub.docker.com/_/ghost/
To run Ghost with a path to your theme, run:

```bash
docker run -d --name casper -v /your/path/here:/var/lib/ghost/content -p 3001:2368 ghost
```

Remember to replace `/your/local/path/` with a path on your local machine to the ghost install content path. 

Ghost should now be available on port `3001`.

