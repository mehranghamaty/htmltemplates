# HTMLTEMPLATES

Inspired from [html-compiler](https://github.com/mehranghamaty/html-compiler). 

A shared library for generating templated html pages.

The intented usage would be as follows:

1. You have folders specified by a file (looks like a toml, but techinically I am not following the exact standard)
```
[config]
folder_to_compile = {folder_to_compile}
template_folder = {template_folder}
output_folder = {output_folder}
string_folder = {string_folder}
```

2. Library offers a class which looks like the following.
```
HTMLTemplates pages = new HTMLTemplates("config.toml");

...
pages.preconfigure(key, value);
...
pages.set_language('EN');
...
pages.render("welcome/hello.html", {...additionalconfiguration});
...
```

To understand how we support multiple languages please see [here](Documentation/SupportedLanguages.md).

3. The pages themselves are formatted like traditional html but with the following phrases replaced when rendered.

```
{{ variable_from_additional_configuration | optional_function | another_optional_function }}
```

To see a list of functions [here](Documentation/OptionalFunctions.md).