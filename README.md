# &lt;lmv-viewer&gt;

A Custom Element for Autodesk's LMV, also officially known as [the View and Data API](http://developer-autodesk.github.io/)

See live demo at http://nopjia.github.io/lmv-viewer/

## Usage

Simply load a file
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

## Example

Try it yourself by pasting this into a blank HTML file
```html
<!DOCTYPE html>
<html>
<head>
  <title>LMV Test</title>

  <!-- include polyfill, eventually this will go away! -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/webcomponentsjs/0.7.3/webcomponents.min.js"></script>

  <!-- include the lmv-viewer element -->
  <link rel="import" href="https://rawgit.com/nopjia/lmv-viewer/master/lmv-viewer.html">
</head>
<body>

  <!-- insert lmv-viewer element -->
  <lmv-viewer url="https://lmv.rocks/data/engineraw/0.svf"></lmv-viewer>

</body>
</html>
```


## License

[BSD 3-Clause License](http://opensource.org/licenses/BSD-3-Clause)
