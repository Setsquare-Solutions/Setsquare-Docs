# Shortcodes

Shortcodes are small pieces of special text that can be inserted into a page to perform more complex functions, that you may not be able to create yourself through the content editor. 

Shortcodes follow the format of a command word enclosed in square brackets with additional information passed using quotation marks. For example:

    [MyCustomCommand parameter1="my custom value" parameter2="another custom value"]

The simplest real example would be the shortcode to display a form. FormDisplay tells the system it needs to output a form, id=”x” tells it which form to output.

    [FormDisplay id="1"]

Shortcodes have to be created individually so you aren’t able to pass any information you like. These will be created per client to achieve specific bespoke functionality.

A list of currently created shortcodes and what can be passed to them is below.

* `[FormDisplay]` - outputs a form. Allowed values:
    * `id=""`       - the ID of the form to output