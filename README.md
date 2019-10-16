# Husky-
### Husky with Eslint and prettier
1) npm install -save --dev husky
2) in package.json add the following -->
  "scripts": {
         "pretest": "./node_modules/.bin/eslint --ignore-path .gitignore . --fix",
    "precommit": "lint-staged && npm test",
    "prettier": "prettier --write src/**/*.{js,css}"
  }, "husky": {
    "hooks": {
      "pre-commit": "npm run pretest && npm run prettier "
    }
  },
