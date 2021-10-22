# OKCTL.io Ghost.io Theme

Based on the DigiDocs theme from Themeforest and the [custom okctl](https://github.com/oslokommune/okctl-ghost-theme) theme by @DanielElisenberg.

## Repository Configuration
The repository is built and deployed using Github Actions, directly to ghost.io, converting the assets/scss/screen.scss file to CSS using Gulp. 

To test locally, you need NPM installed, then install the gulp CLI globally using:
```bash
npm install gulp-cli -g
```

You can then build the code using:

```bash
gulp build
```