# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    A visual hierarchy is that you could have an index page that loads a list
    component.  The list component has some titles and descriptions beneath that,
    so you would have to create component/template files for the list itself
    and then nest component/template files for the titles and descriptions
    of the list items.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
  ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
  The template and the component files are edited.  With the template, it determines
  what specific data will be displayed and potentially any actions on that
  data. The component file determines the default settings for that data, for example
  a default could be that each data element is wrapped in a div, or that it turns
  on or off a class name based upon an action done to the data.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each model as |my-contact|}}
      {{contacts my-contact=my-contact}}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
      {{#each my-contact.my-phone as |phone|}}
        {{my-contact/phone phone=phone}}
      {{/each}}
    ```
