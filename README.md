# RSelenium

forked from [https://github.com/ropensci/RSelenium](https://github.com/ropensci/RSelenium)

## Differences from origin

- Not use httr::VERB option `encode = "json"`
- Set custom header `Content-Type: application/json; charset=utf-8;`

To avoid error that origined from requesting JSON MIME Type without `charset=utf-8` header.

## Usage

Set global variables to show raw responses.

```{r}
rselenium_show_raw_response = T;
rselenium_show_raw_response_debug_function = function(resContent) { View(resContent) };
```
