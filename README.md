# Hello Accusoft PDF Viewer via CDN

![Accusoft PDF Viewer Illustration](https://resource.accusoft.com/r01/wp-content/uploads/APDFV_Professional-Version-turq-730-banner.png)

Minimal example of an HTML page which uses [Accusoft PDF
Viewer](https://www.npmjs.com/package/@accusoft/pdf-viewer) via a `<script>` tag
and CDN URL to display a PDF.

## Live Example

[Click here to try the sample now in your browser.](https://accusoft.github.io/hello-accusoft-pdf-viewer-via-cdn/)

## Running Locally

Clone this repo and `cd` into the directory:

    git clone git@github.com:Accusoft/hello-accusoft-pdf-viewer-via-cdn.git
    cd hello-accusoft-pdf-viewer-via-cdn

Launch a local web server for the directory and open a browser to view the
sample. For example, if you have npm installed, you can run:

    npx serve

This will start a local web server running at (typically)
`http://localhost:5000`. Open this URL in your browser to view the sample.

## Evaluation of All Features

This sample is set up for an evaluation of all features. In this mode,
all functionality is available without a license, but the document will
show a watermark on it. You can find out more about the available control
[here](https://help.accusoft.com/accusoft-pdf-viewer/latest/api/classes/pdfviewercontrol.html#create).

The code to enable features looks like this:

```javascript
await window.Accusoft.PdfViewerControl.create({
  sourceDocument: sourceDocument,
  container: document.getElementById('viewer-container'),

  // Evaluate Professional features (page contents will be watermarked)
  licenseKey: 'eval',

  // Configure the UI:
  allowedControls: {
    // Enable or disable annotation tools (all false by default):
    annotationList: true,
    ellipseTool: true,
    freehandDrawingTool: true,
    freehandSignatureTool: true,
    lineTool: true,
    outline: true,
    rectangleTool: true,
    textHighlightTool: true,
    thumbnails: true,

    // Enable or disable other parts of the UI (all true by default):
    fullScreenToggle: true,
    nextAndPreviousPageButtons: true,
    pageNumberAndCount: true,
    printing: true,
    search: true,
    thumbnails: true,
    zoomInAndOutButtons: true
  }
});
```

## About Accusoft PDF Viewer

Note this example utilizes the Standard version of Accusoft PDF Viewer, which
is completely free to use. Our enhanced features like annotation and eSignature
are part of our Professional Version which you will need a
[trial key](https://www.accusoft.com/products/pdf-collection/accusoft-pdf-viewer-professional-trial)
to evaluate. You can also email info@accusoft.com or call us at 1-800-875-7009
for more information on our paid product and licensing.
