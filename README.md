# jquery.panel.js
Additional functionallity for the Bootstrap 3 Panel

## Installation

Include the script *after* the jQuery library

```html
<script src="/path/to/jquery.panel.js"></script>
```

## Usage

Initialize the plugin and put the code inside the jQuery document.ready callback like here:

```html
<div class="panel panel-default">
  <div class="panel-heading">
    <h3 class="panel-title">My Panel</h3>
  </div>
  <div class="panel-body">
    My Panel content
  </div>
</div>
```

```javascript
$(function(){        
    // Example 1: Call without configuration (Individual configuration could be done in HTML via data- Attributes)
    $('.panel').panel();
    
    // Example 2: Put all configuration in Javascript
    $('.panel').panel({
      url: '/user/profile?id=0815',
      collapsible: true,
      collapsed: false,
      autorefresh: 10
    });
});
```

## Panel Configuration

To configure an environment for usage in your application, the following options can be used:

### collapsible

When true, adds an chevron icon to the header to toggle between collapsed and uncollapsed state.

### collapsed

Defines the initial state of the panel. Ignored if <code>collapsible</code> is <code>false</code>. If no <code>collapsed</code> is defined, but an url is defined, the panel starts collapsed and uncollapses as soon as any content is received.

### url 

An url to load HTML contents via XHR.

### autorefresh

Interval in seconds to reload content via given <code>url</code>.

## Authors

[K. Feldmaier](https://github.com/eddieconnecti)
