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
<!-- Simple Panel without data- Attributes; Configuration is set in Javascript -->
<div class="panel panel-default">
  <div class="panel-heading">
    <h3 class="panel-title">My Panel</h3>
  </div>
  <div class="panel-body">
    My Panel content
  </div>
</div>

<!-- Panel using data- Attributes for individual configuration -->
<div class="panel panel-default" data-url="/user/profile?id=0815" data-collapsible="true" data-collapsed="false" data-autorefresh="10">
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

Two ways to configure jquery.panel.js:
- Passing Configuration Parameters in Javascript
- Adding data- Attributes to the Panel Element

Decide, how you want to integrate the Panel: If all Panels on one page share the same configuration, use Javascript. If you have multiple Panels with different options, use the HTML Initialisation. You can also use a Mix of both, ie. it could make sense to only define the url per data- Attribute and setup all the other parameters in Javascript. 

### collapsible

When true, adds an chevron icon to the header to toggle between collapsed and uncollapsed state.

### collapsed

Defines the initial state of the panel. Ignored if <code>collapsible</code> is <code>false</code>. If no <code>collapsed</code> is defined, but an url is defined, the panel starts collapsed and uncollapses as soon as any content is received.

### url 

An url to load HTML contents via XHR.

### autorefresh

Interval in seconds to reload content via given <code>url</code>.

## Requires

- [Bootstrap 3](http://getbootstrap.com/)
- [jQuery 1.11.2](https://jquery.com/)

## Authors

[K. Feldmaier](https://github.com/eddieconnecti)
