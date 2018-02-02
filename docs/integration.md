---
id: integration
title: Library Integration
---
**************************************************************************************************
Table of Contents
- [Integration with Angular](#integration-with-angular)
- [Integration with Webpack/Typescript](#integration-with-webpacktypescript)
**************************************************************************************************

## Integration with Angular

Set the browser mode option so the library will use `window` blob file saving instead of detecting
your app as a Node.js app (Node apps utlize `fs.writeFile` or file streaming).  
* `pptx.setBrowser(true);`

[See Issue #220 for more information](https://github.com/gitbrent/PptxGenJS/issues/220)

## Integration with Webpack/Typescript

Add this to your webpack config to avoid a module resolution error:
* `node: { fs: "empty" }`  

Set browser mode so files will save as blobs via browser:
* `pptx.setBrowser(true);`

[See Issue #72 for more information](https://github.com/gitbrent/PptxGenJS/issues/72)