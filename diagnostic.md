# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    http://emberigniter.com/communication-between-distant-components/
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    The component.js file and a template.hbs file located within the component
    directory that gets generated when you run ember g component. The responsibility
    of the template is to display/render the data received from the route and the component
    file holds the UI/Actions that create the "controls" in the application.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html

    {{#each model as |contact|}}
      {{my-contact contact=contact}}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each myPhones as |myPhone|}}
      {{my-phone phone=myPhone}}
    {{/each}}
    ```
