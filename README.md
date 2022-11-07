# RSelenium

forked from [https://github.com/ropensci/RSelenium](https://github.com/ropensci/RSelenium)

## Differences from origin

- Not use httr::VERB option `encode = "json"`
- Set custom header `Content-Type: application/json; charset=utf-8;`

To avoid error that origined from requesting JSON MIME Type request without `charset=utf-8` header.

## Installation

```{r}
install.packages('devtools') # needs devtools
library(devtools)
install_github('khskeb0513/RSelenium') # install package from github repo
library(RSelenium)
```

If you had installed RSelenium from CRAN already...

```{r}
remove.packages('RSelenium') # remove installed package
detach('package:RSelenium', unload = T) # unload package from memory
```

then follow upper steps.

## Usage

Set global variables to show raw responses.

```{r}
rselenium_show_raw_response = T;
rselenium_show_raw_response_debug_function = function(resContent) { View(resContent) };
```
