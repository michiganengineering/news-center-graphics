# CoE News Center Graphics

This is the repository for the News Center Graphics team. As of this writing (Jan 2018), the repository only contains ai2html and yet may house other graphics or animations as we develop them for the News Center.

## ai2html

ai2html is an open-source script for Adobe Illustrator originally developed by The New York Times news development team. It converts an Illustrator document into HTML and CSS. The embeds are hosted as GitHub pages – this may change in the future.

### Installing ai2html

Download the latest version of the script called `ai2html.js` and saving the file to your computer. This version of the script contains a custom font array with the fonts that we use in the News Center. When updating to the latest script pulled from [here](https://github.com/newsdev/ai2html), be sure to preserve the custom array starting from line 309.

Move the `ai2html.js` file into the Illustrator folder where scripts are located. For example, on a Mac running Adobe Illustrator CC 201x, the path would be:

```
/Applications/Adobe Illustrator CC 2018/Presets/en_US/Scripts/ai2html.js
```

### How to use ai2html

#### Basic instructions
1. Create your Illustrator artwork.
  * Size the artboard to the dimensions that you want the div to appear on the web page.
  * Make sure your Document Color Mode is set to RGB.
  * Make sure your document is saved.
  * Use Open San Regular or Open Sans Bold for labels.
2. Run the script by choosing: File > Scripts > ai2html
3. Go to the folder containing your Illustrator file. Inside will be a folder called `embed`. Open the html files in your browser to preview your output. This is a partial so it will need `html`, `body`, etc. for it to be semantically correct.

Currently, we are making heavy use of custom settings. For example, using the `ai2html-html` setting will insert custom html at the end of the document. Here's an example where we insert some scripts needed to display the iframe embeds properly:
```
ai2html-html
<div <%=caption_class%>><%=credit%></div>
<script type="text/javascript" src="../../js/resizer-script.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/3.5.16/iframeResizer.contentWindow.min.js"></script>
```

For more in-depth instructions and information on the various settings, go [here](http://ai2html.org/#how-to-use-ai2html). The Illustrator document in the example embed also has custom settings that can be used as a template. Note that there are four artboards. Those (loosely) correspond to the breakpoints in the News Center. They may work in the department and college sites, but that has not been tested.

For some proof-of-concepts in our News Center, several appear in [this page](https://newsdev.engin.umich.edu/features/internal-feature-test/).

## Haiku animations

Tentatively testing this. It may end up being something else. [TK TK TK TK](https://www.haiku.ai/) 

## License

TK TK TK