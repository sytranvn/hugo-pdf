# hugo-pdf
This shortcode allows you to add PDF file to your pages using browser native 
PDF renderer. Therefore, no additional Javascripts needed.

# Installation
Copy the `pdf.html` to your `layouts/shortcodes/` website directory.
Or run follow commands from you website directory.
Make a directory if not exist.
```
mkdir -p layouts/shortcodes
```
Download `pdf.html` file.
```
# using curl
curl -o layouts/shortcodes/pdf.html https://raw.githubusercontent.com/sytranvn/hugo-pdf/master/pdf.html
# or wget
wget https://raw.githubusercontent.com/sytranvn/hugo-pdf/master/pdf.html -O layouts/shortcodes/pdf.html 
```

# Usage
```
{{< pdf url="./path/to/example.pdf" >}}

# Adjust size
{{< pdf url="./path/to/example.pdf" width="100%" height="500px" >}}

# Adjust zoom level and page

{{< pdf url="./path/to/example.pdf#view=Fit&page=2" width="100%" height="500px" >}}
```

You can also add parameters to url to customize PDF viewer.
| Parameters  | Value  | Description  | Browser  |
|---|---|---|---|
| `toolbar`  | `1`,`0`  | Toggle toolbar  | Chrome  |
| `view`  | `Fit`, `FitH`, `FitV`  | Fit content (both, horizontal, vertical)  | Chrome  |
| `zoom`  | `number`  | Zoom by `n%`  | Chrome, FF  |
| `page`  | `number`  | Select page to render  | Chrome, FF, Safari  |
| `nameddest`  | `string`  | Anchor position like header | Chrome  |
