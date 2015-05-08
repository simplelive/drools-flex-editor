# Release 0.5 #
The current release only includes the Flex part of the editor. Subsequent releases will include the necessary server side code for compiling, and code completion.


# Integration #
You can integrate the Flash file directly into your app. The easiest way is to take a look at the sample program: **orangemile-editor\bin-debug\main.html**

The flash program has certain integration points:

**Save button** - calls a save function on the javascript program passing in the ruletext.

```
  function save(ruleText) {
    alert("Called from Flex Editor: " + ruleText);
  }
```

The following parameters can be passed into the flash file to override local defaults.
  * languageElementsUrl - default: data/language-elements.xml
  * codeCompleteUrl - default: data/code-complete.xml
  * compileUrl - default: data/compile-response.xml