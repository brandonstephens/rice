# 🍚 Rice Calculator

Rice calculator for electric pressure cookers.

[![Netlify Status](https://api.netlify.com/api/v1/badges/60062fed-3093-4244-bccf-e2d571fede7b/deploy-status)](https://app.netlify.com/sites/unruffled-gates-4f8ba8/deploys)

## 💾 Installation

1. `nvm use`
2. `npm install`
3. `npm start`
4. <http://localhost:8081>

## 🖥 Commands

### dev

1. `npm start`
2. <http://localhost:8081>

### build

Build production version of the site.

1. `npm run build`
2. output goes to `./dist`

### serve

Serve the `./dist` directory.

1. `npm run serve`
2. <http://localhost:3000>

### clean

Delete the `./dist` folder and `./src/styles/`.

1. `npm run clean`

### Notes on build process

#### Dev

1. Gulp runs PostCSS to build Tailwind to `./src/styles.css`
2. Eleventy runs and links to css at `./src/styles.css`
3. Gulp watches for changes to `.src/postcss/`
4. Eleventy watches for changes to lots of files including the output of gulp css to `.src/styles`

#### Production

1. CSS is built via PostCSS in production mode (which purges unused Tailwind classes) via Gulp
2. Then Eleventy runs in production mode
3. Gulp inlines and minifys CSS, JS, HTML from the eleventy output

## ♿️ Accessibility

- [Lighthouse](https://developers.google.com/speed/pagespeed/insights/?url=https://rice.bsteph.com)
- [Web accessibility evaluation tool](https://wave.webaim.org/report#/https://rice.bsteph.com)

**Note on viewport**  
To get 100% on accessibility under the Lighthouse metric you need to update the `viewport` meta tag to be:

```
<meta name="viewport" content="width=device-width, minimum-scale=1, maximum-scale=5" />
```

I've chosen not to do this as it causes the site to zoom in frequently while tapping the UI.

## 📚 References

- [eleventy](https://www.11ty.dev)
- [tailwindcss](https://tailwindcss.com)
- [alpinejs](https://github.com/alpinejs/alpine)
- [gulp](https://gulpjs.com)
- [liquid](https://liquidjs.com)
- [nvm](https://github.com/nvm-sh/nvm)

## 🌎 Hosting

- CI & Hosting on [Netlify](https://www.netlify.com).
- [GoSquared](https://www.gosquared.com) analytics added as post processing step in Netlify.

## 🗺 Roadmap

- [x] replace name in readme
- [x] add copy instructions
- [x] add ratio components
- [x] try alpine and add inputs to update ratio
- [x] style it
- [x] update site name in `./src/_data/site.js`
- [x] add apple touch icon to `./src/assets`
- [x] add favicon to `./src/assets`
- [x] add to netlify
- [x] add netlify badge to project
- [x] add gosquared analytics
- [x] add url to Lighthouse in Accessibility
- [x] add url to WAVE in Accessibility

---

If you find this project useful you can donate:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/G2G33AMQO)
