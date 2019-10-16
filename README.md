# Husky-
### Husky with Eslint
1) npm install -save --dev husky
2) in package.json add the following -->
  "scripts": {
    "pretest": "./node_modules/.bin/eslint --ignore-path .gitignore . --fix",
    "precommit": "lint-staged && npm test"
  },  "husky": {
    "hooks": {
      "pre-commit": "npm run pretest"
    }
