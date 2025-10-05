# Bet Prophet 
  
Created to treat bettors fairly.
  
## Getting Started


These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites


- Node
- Yarn

### Installing

A step by step series of examples that tell you how to get a development env running. Make sure to copy the `.env.test` file to a `.env` file in the root.

```
# install dependencies
$ yarn

# serve with hot reload at localhost:3000
$ yarn dev
```

## E2E Testing

Cypress is the front end testing tool used for the app it provides different kinds of testing e2e, integration and unit tests.

```
# run all tests
yarn e2e

# open cypress gui
yarn e2e:open
```

## Environments

- [Staging](https://staging.betprophet.co/) - For developer to deploy features

```
# add changes to main
git push origin main
```

- [Test](https://test.betprophet.co/) - For QA to test features / regression test

```
# tag or point a specific spot in git history
git tag testing.2022.$(week).1
git push origin testing.2022.$(week).1
```

- [Sandbox](https://sandbox.betprophet.co/) - For DGE to test and demo for customers

```
# tag or point a specific spot in git history
git tag sandbox.2022.$(week).1
git push origin sandbox.2022.$(week).1
```

- [Production](https://www.prophetx.co/)

```
# tag or point a specific spot in git history
git tag frontend.2022.$(week).1
git push origin frontend.2022.$(week).1
```

## Built With

- [Nuxt](https://nuxtjs.org/) - The FE framework used
- [Tailwind](https://tailwindcss.com/) - The CSS framework used
  <!-- * [ESLint](https://eslint.org/) - The tool to analyze and find code problems with JS  -->

## Project Structure

```
├── api                     # centralized api connections from BE services
├── assets                  # uncompiled assets such as your styles, images, or fonts
├── components              # vue components
├── constants               # static variables
├── layouts                 # vue layout
├── middleware              # custom functions that can be run before rendering a page
├── mixins                  # vue mixins
├── pages                   # contains your application's views and routes
├── plugins                 # contains plugins and to inject functions or constants
├── static                  # static files and directly mapped from server
├── store                   # contains your vuex files
├── test                    # cypress
│   └── e2e                 # e2e test cases
```

## Authors

- **Paulo Trajano** - _Lead Developer_ - [paulotra](https://github.com/paulotra)
- **Heindrick Dumdum** - _Front End Developer_
- **Viet Mai** - _Front End Developer_
- **Son Nguy** - _Front End Developer_

## Dependencies

- [idle-vue](https://www.npmjs.com/package/idle-vue) - Detects when the user hasn't interacted with your app
- [lodash-es](http://lodash.com/) - Provides individual lodash utilities
- [v-money](http://lodash.com/) - Masking for money format
- [moment](https://momentjs.com/) - Date parser
- [cookie-universal-nuxt]() - To set browser's cookies (e.g. variables)
- [vue-countup-v2]() - To see movement in money changes
- [vue-clipboard2]() - Copy and paste plugin
- [v-tooltip]() - Tooltip ui plugin
- [v-money]() - Mask to money format for inputs
- [vue-avatar]() - Generate initials for avatar icon
- [vue-flickity]() - Carousel plugin
- [vue-instantsearch]() - Algolia search tool
- [vue-notification]() - Toasters used for notification
- [vue-select]() - Select input plugin
- [vue-the-mask]() - Provides a strong masking feature for inputs
