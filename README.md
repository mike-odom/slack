# Slack Customization

A place to store .css for custom slack styling that can be served up via http

*(This will need to be redone after every slack update.)*

## Directions

Append the following code snippet to `C:\Users\<username>\AppData\Local\slack\app-3.0.0\resources\app.asar.unpacked/src/static/ssb-interop.js`:

```javascript
document.addEventListener('DOMContentLoaded', function() {

 $.ajax({
   url: 'https://raw.githubusercontent.com/jon-is-learning/slack/master/darkSlack.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
```

## Sources ##

 - ~~[Hide Sidebar](http://www.0atman.com/remove-slacks-sidebar.html "start of rabbit hole")~~
 - [Updated Hide Sidebar](https://userstyles.org/styles/119991/slack-hide-sidebar-when-window-is-narrow "works with 3.0.0")
 - [Add custom CSS to windows desktop version](https://github.com/laCour/slack-night-mode/issues/73#issuecomment-287467332 "directions for fetching custom URL at load")
 - [Original CSS source](https://cdn.rawgit.com/laCour/slack-night-mode/master/css/raw/black.css "sourced from previous link directions")
