---
description: more text
---

# text

## AsText(html) <a href="#astext" id="astext"></a>

### Result:

Returns a text that includes all HTML tags

### Parameters:

| Parameter | Mandatory | Description                                 |
| --------- | --------- | ------------------------------------------- |
| html      | Yes       | Html input that you want to convert to text |

&#x20;

### Examples:

| S.No. | Expression                                                | Result                                                                   |
| ----- | --------------------------------------------------------- | ------------------------------------------------------------------------ |
| 1     | AsText(RichText("\<html>\<body>Welcome\</body>\</html>")) | "\<html>\<body>Welcome\</body>\</html>"                                  |
| 2     | AsText(RichText("Welcome"))                               | "Welcome"                                                                |
| 3     | AsText("\<html>\<body>Welcome\</body>\</html>")           | This expression is invalid because the parameter is text instead of HTML |

&#x20;
