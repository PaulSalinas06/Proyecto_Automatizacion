# Proyecto_Automatizacion
Configura un nuevo proyecto Node.js:
  mkdir todo-automation
  cd todo-automation
  npm init -y
Instala CypressJS y Cucumber, así como otras dependencias necesarias:
  npm install cypress cucumber cypress-cucumber-preprocessor --save-dev
Configura Cypress y Cucumber. Crea un archivo cypress/plugins/index.js:
  const cucumber = require('cypress-cucumber-preprocessor').default;
  module.exports = (on, config) => {
  on('file:preprocessor', cucumber());
  };

Configura Cypress para que use Cucumber en cypress.json:
  {
  "testFiles": "**/*.feature",
  "pluginsFile": "cypress/plugins/index.js"
  }
Ejecuta Cypress con el siguiente comando:
  npx cypress open
