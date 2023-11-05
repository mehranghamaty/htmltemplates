1. `prerender`

tags with prerender search the folder provided at the path in the confiration file to prerender items. 

In order to prerender and cache values we can use:

```
{{ variable_name | prerenderable }}
```

Although we aim to keep things in memory to minimize calls to translation services we cache things on disk. 

Any of these tags will be prerendered and cached. 