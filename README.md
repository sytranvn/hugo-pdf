# hugo-pdf
This shortcode allows you to add PDF file to your pages using browser native 
PDF renderer. Therefore, no additional Javascripts needed.

# Installation
## Option 1
Copy the only `layouts/shortcodes/pdf.html` file to your `layouts/shortcodes/` website directory and you are good to go.

## Option 2
Or use this as a theme.
- add this to your `config.toml` theme
```yml
theme = "hugo-pdf"
# use with existing theme
theme = [current-theme,hugo-pdf]
```
- And clone this repo to your theme directory as submodule.
```shell
git submodule add -f --name hugo-pdf https://github.com/sytranvn/hugo-pdf.git themes/hugo-pdf
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

# Issues
On mobile webview, this solution does not work. User need to download open
the pdf them self. 