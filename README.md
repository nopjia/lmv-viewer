# &lt;lmv-viewer&gt;

A Custom Element for Autodesk's LMV, also officially known as [the View and Data API](http://developer-autodesk.github.io/)

```html
<lmv-viewer url="https://lmv.rocks/data/engineraw/0.svf"></lmv-viewer>
```

See demo at http://nopjia.github.io/lmv-viewer/

See more samples and information for LMV at http://lmv.rocks/

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install lmv-viewer
```

Or [download as ZIP](https://github.com/nopjia/lmv-viewer/archive/master.zip).

## Usage

1. Import polyfill:
    ```html
    <script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>
    ```

1. Import firefly.js
    ```html
    <script src="http://autodeskviewer.com/viewers-dev/latest/firefly.js"></script>
    ```
    And optionally import extensions
    ```html
    <script src="http://autodeskviewer.com/viewers-dev/latest/firefly-extensions.js"></script>
    ```

1. Import &lt;lmv-viewer&gt; element:
    ```html
    <link rel="import" href="bower_components/lmv-viewer/lmv-viewer.html">
    ```

1. Load a file
    ```html
    <lmv-viewer url="https://lmv.rocks/data/engineraw/0.svf"></lmv-viewer>
    ```
    Or load URN with your access token from Autodesk server
    ```html
    <lmv-viewer url="urn:dXJuOmFkc2sub2JqZWN0czpvcy5vYmplY3Q6bm9wL0FyYm9yUHJlc3MuZHdm" token="7twj3okWPRkbBMtpfUSN5hZkcAkv"></lmv-viewer>
    ```

## Attributes

Attribute | Options  | Description
---       | ---      | ---
`url`     | *string* | URL of document or model to load
`token`   | *string* | (Optional) Access token required to load URL from Autodesk servers
`env`     | *string* | (Optional) Server environment, defaults to "AutodeskProduction"

## Properties

Property  | Description
---       | ---
`viewer`  | The Viewer3D instance. Use this to access the LMV [Viewing API](https://s3.amazonaws.com/autodesk.viewingservice.viewers.prod/1.2.13/docs/index.html).
`doc`     | The loaded document, if exists. See Autodesk.Viewing.Document _(TODO: Link?)_

## Example

Try it yourself by pasting this into a blank HTML file
```html
<!DOCTYPE html>
<html>
<head>
  <title>LMV Test</title>

  <!-- Import polyfill -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/webcomponentsjs/0.7.3/webcomponents.min.js"></script>

  <!-- Import firefly.js -->
  <script src="http://autodeskviewer.com/viewers-dev/latest/firefly.js"></script>

  <!-- Import lmv-viewer element -->
  <link rel="import" href="https://rawgit.com/nopjia/lmv-viewer/develop/lmv-viewer.html">
</head>
<body>

  <!-- insert lmv-viewer element -->
  <lmv-viewer url="https://lmv.rocks/data/engineraw/0.svf"></lmv-viewer>

</body>
</html>
```
