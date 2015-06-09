# &lt;lmv-viewer&gt;

LMV Viewer Custom Element

## Attributes

Attribute | Options  | Description
---       | ---      | ---
`url`     | *string* | URL of document or model to load
`token`   | *string* | (Optional) Access token required to load URL from Autodesk servers
`env`     | *string* | (Optional) Server environment, defaults to "AutodeskProduction"

## Properties

Property  | Description
---       | ---
`viewer`  | The Viewer3D instance. Use this access the LMV [Viewing API](https://s3.amazonaws.com/autodesk.viewingservice.viewers.prod/1.2.13/docs/index.html).

## License

[BSD 3-Clause License](http://opensource.org/licenses/BSD-3-Clause)
