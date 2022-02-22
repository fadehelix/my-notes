## Guides
[Readme from cypress-cucumber-preprocessor](https://github.com/TheBrainFamily/cypress-cucumber-preprocessor)
[How to run Cypress with Cucumber](https://www.browserstack.com/guide/how-to-run-cypress-cucumber-test)

## Example
[Scenarios in Bloxt](https://github.com/fadehelix/bloxt/tree/master/cypress/integration) 

## Setup VSCode

^45766b

1. Install [Cucumber Extension](https://marketplace.visualstudio.com/items?itemName=alexkrechik.cucumberautocomplete)
2. Enable intelisense by edit `settings.json`: 
```javascript
"cucumberautocomplete.steps": ["cypress/integration/**/*.js"]
``````
3. 



## Q&A
### ESLint error: `cy is not defined`
Install `eslint-plugin-cypress`
Edit  `.eslintrc.json`

```javascript
{
  "extends": [
    "plugin:cypress/recommended"
  ]
}
```