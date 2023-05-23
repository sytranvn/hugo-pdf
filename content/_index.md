---
weight: 1
title: "Hugo PDF"
git_repo: https://github.com/sytranvn/hugo-pdf
summary: "This shortcode allows you to add PDF file to your pages using browser native PDF renderer. Therefore, no additional Javascripts needed."
type: single
---

This shortcode allows you to add PDF file to your pages using browser native 
PDF renderer. Therefore, no additional Javascripts needed.

# Installation
## Option 1
Copy the only `layouts/shortcodes/pdf.html` file to your `layouts/shortcodes/` website directory and you are good to go.

## Option 2
```yml
theme = "hugo-pdf"
# use with existing theme
theme = [current-theme,hugo-pdf]
```

```shell
git submodule add -f --name hugo-pdf https://github.com/sytranvn/hugo-pdf.git themes/hugo-pdf
```

Or use this as a theme.
- Add this to your `config.toml` theme
- And clone this repo to your theme directory as submodule.


# Usage

## Default
```md
{{</* pdf src="./path/to/example.pdf" */>}}
```

{{< pdf src="landscape.pdf" >}}


## Customize size

```md
# Adjust size
{{</* pdf src="./path/to/example.pdf" width="30%" height="400px" */>}}
```

{{< pdf src="landscape.pdf" width="40%" height="400px" >}}


## Zoom and page
```md
# Adjust zoom level and page
{{</* pdf src="./path/to/example.pdf#view=Fit&page=1" width="100%" height="500px" */>}}
```

{{< pdf src="landscape.pdf#view=Fit" width="100%" height="500px" >}} 

## More options
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





