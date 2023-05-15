# README.md

> ## This is a stack README file displayed on stack details pages. Edit it to showcase your stack, tell people what can be done with it and how to used it.

## Stack templates READMEs

When using stack templates, the README file of the template will be copied over to the stacks generated.  
Like for other files of a template, it is possible to use Jinja templating inside the template `README.md` file. It will be compiled when users generate a stack from it.

Some variables are exposed and can be used in READMEs to generate dynamic content.

```jinja
{% raw -%}
Printing a variable value: {{ stack_usecase }}

{% if stack_usecase == "foo" %}
  Using expressions
{% endif %}
{%- endraw %}
```

**Available variables**

| Name | Description |
|--|--|
| `stack_usecase` | The key of the selected use case |
| `stack_author` | The username of the user who creates the stack |
| `stack_canonical` | The stack canonical filled in by the user |
| `stack_path` | The path of the generated stack in the catalog repository |
| `scs_canonical` | The canonical of the target catalog repository |
| `scs_cred_path` | The path in Vault of the target catalog repository credential |
| `scs_cred_type` | The type of the target catalog repository credential (`ssh` or `http`) |
| `api_url` | {{ api_url }} | The URL of the Cycloid API |
