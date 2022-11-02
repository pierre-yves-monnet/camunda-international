# camunda-international

This is a C7 camunda server using the different language

See https://github.com/camunda-consulting/camunda-7-code-examples/blob/master/snippets/springboot-customized-webapps/

# use it
1/ Start it
2/ **Change the language in your browser** to access Cockpit/TaskList/Admin in a different language

# Copy the last version of dictionary
Copy from (Camunda Web Translation)[https://github.com/camunda/camunda-webapp-translations] files

Copy admin/*.json to src/main/resources/META-INF/resources/webjars/camunda/app/admin/locales
Copy cockpit/*.json to src/main/resources/META-INF/resources/webjars/camunda/app/cockpit/locales
Copy tasklist/*.json to src/main/resources/META-INF/resources/webjars/camunda/app/tasklist/locales

# What is the configuration?
https://forum.camunda.io/t/spring-boot-webapps-localization-customization/4915/2

Then, 
1/ Create src/main/resources/META-INF/resources/webjars/camunda/app
2/ Create subfolders admin/cockpit/admin
3/ In each subfolder, add scripts/config.js
 In the config.js, reference all external language
``````
` 'locales': {
    'availableLocales': ['fr', 'en', 'de'],
    'fallbackLocale': 'en'
  },
``````

4/ In each subfolder, add locales/<lang>.json

Get each dictionary (<lang>.json) from the Camunda Web Translation

You have in final
src/main/resources/META-INF/resources/webjars/camunda/app/admin/script/config.js
src/main/resources/META-INF/resources/webjars/camunda/app/admin/local/fr.json

src/main/resources/META-INF/resources/webjars/camunda/app/cockpit/script/config.js
src/main/resources/META-INF/resources/webjars/camunda/app/cockpit/local/fr.json

src/main/resources/META-INF/resources/webjars/camunda/app/tasklist/script/config.js
src/main/resources/META-INF/resources/webjars/camunda/app/tasklist/local/fr.json

