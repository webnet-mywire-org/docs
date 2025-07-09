# <img src="https://raw.githubusercontent.com/webnet-mywire-org/docs/refs/heads/master/image/favicon.svg" alt="Logo" width="26px" /> WebNet JavaScript Library Documentation  

Welcome to the WebNet JavaScript Library Documentation, your comprehensive guide to integrating and utilizing the powerful features of the WebNet platform. This documentation provides detailed information on endpoints, request/response formats, and usage examples to help developers seamlessly interact with our services.


## URL

URL: https://assets.webnet.mywire.org/js/WebNet.js

HTML:
```html
<script src="https://assets.webnet.mywire.org/js/WebNet.js"></script>
```

## wn.ui (User Interface) 

### wn.ui.theme()

```void: theme(void)```

Set the website DaisyUI theme, initially performed on web page loading.

### wn.ui.setTheme()

```string: theme(theme: string) ```

Change and set the website theme.

### wn.ui.getThemes()

```array: getTheme(void) ```

Get a list of available themes.

### wn.ui.getUIID()

```string: getUIID(void)```

Get a UIID for an element in the UI, for example: "uiid-ia30fdnq9f".

### wn.ui.toast()

```void: wn.ui.toast(string: type = 'info',string: message = "",integer: duration = 3000,boolean: fill = false, boolean: soft = false)```

Display a toast message. Accepted types are: "info", "error", "success", "warning". The fill and soft options are for styling.

To work, the body needs this element:
```html
<div class="toast" id="toast"></div>
```


