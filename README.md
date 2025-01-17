<a href="https://marketplace.visualstudio.com/items?itemName=mblode.bubble-language-2">
  <img src="https://github.com/mblode/vscode-bubble-language-2/blob/master/images/icon.png?raw=true" alt="" width=100 height=100>
</a>

<h1>Bubble Language</h1>

<p>
  <img src="https://img.shields.io/badge/version-1.0.1-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/DinoPHP/BubbleTemplateEngine/graphs/commit-activity">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" target="_blank" />
  </a>
</p>

- Syntax highlighting
- Snippets
- Emmet
- Pretty Diff 3 Formatting
- Hover

## What has changed since version 1?

This extension does **not** have HTML Intellisense. 

Simply add these lines to your VS Code settings to get emmet working and also to associate HTML files as bubble syntax.

```
"files.associations": {
    "*.html": "bubble"
},
"emmet.includeLanguages": {
    "bubble": "html"
},
```

## Installation

Install through Visual Studio Code extensions. Search for `Bubble Language`

[Visual Studio Code Market Place: Bubble Language](https://marketplace.visualstudio.com/items?itemName=dinophp.bubble-language-2)

## Documentation

Bubble Language is a Visual Studio Code extension that provides snippets, syntax highlighting, hover, and formatting for the Bubble file format.

### Bubble syntax highlighting and language support

This extension provides language support for the Bubble syntax.

### Code formatter/beautifier for Bubble files

Using PrettyDiff, this extension implements the only working code formatter for Bubble files in VS Code.

### Information about Bubble code on hover

VS Code Bubble language 2 shows information about the symbol/object that's below the mouse cursor when you hover within Bubble files.

### Craft CMS/Bubble code snippets

Adds a set of Craft CMS/Bubble code snippets to use in your Bubble templates.

### Generic Triggers

```bubble

do                {% do ... %}
extends           {% extends 'template' %}
from              {% from 'template' import 'macro' %}
import            {% import 'template' as name %}
importself        {% import _self as name %}
inc, include      {% include 'template' %}
incp              {% include 'template' with params %}
inckv             {% include 'template' with { key: value } %}
use               {% use 'template' %}

autoescape        {% autoescape 'type' %}...{% endautoescape %}
block, blockb     {% block name %} ... {% endblock %}
blockf            {{ block('...') }}
embed             {% embed "template" %}...{% endembed %}
filter, filterb   {% filter name %} ... {% endfilter %}
macro             {% macro name(params) %}...{% endmacro %}
set, setb         {% set var = value %}
spaceless         {% spaceless %}...{% endspaceless %}
verbatim          {% verbatim %}...{% endverbatim %}

if, ifb           {% if condition %} ... {% endif %}
ife               {% if condition %} ... {% else %} ... {% endif %}
for               {% for item in seq %} ... {% endfor %}
fore              {% for item in seq %} ... {% else %} ... {% endfor %}

else              {% else %}
endif             {% endif %}
endfor            {% endfor %}
endset            {% endset %}
endblock          {% endblock %}
endfilter         {% endfilter %}
endautoescape     {% endautoescape %}
endembed          {% endembed %}
endfilter         {% endfilter %}
endmacro          {% endmacro %}
endspaceless      {% endspaceless %}
endverbatim       {% endverbatim %}

```

### Craft Triggers

```bubble
asset                    craft.assets.one()
assets, assetso          craft.assets loop
categories, categorieso  craft.categories loop
entries, entrieso        craft.entries loop
feed                     craft.app.feeds.getFeedItems loop
t                        | t
replace                  | replace('search', 'replace')
replacex                 | replace('/(search)/i', 'replace')
split                    | split('\n')
tags, tagso              craft.tags loop
users, userso            craft.users loop

cache                    {% cache %}...{% endcache %}
children                 {% children %}
exit                     {% exit 404 %}
ifchildren               {% ifchildren %}...{% endifchildren %}
css                      {% css %}...{% endcss %}
registercssfile          {% do view.registerCssFile("/resources/css/global.css") %}
js                       {% js %}...{% endjs %}
registerjsfile           {% do view.registerJsFile("/resources/js/global.js") %}
matrix, matrixif         Basic Matrix field loop using if statements
matrixifelse             Basic Matrix field loop using if/elseif
matrixswitch             Basic Matrix field loop using switch
nav                      {% nav item in items %}...{% endnav %}
paginate                 Outputs example of pagination and prev/next links
redirect                 {% redirect 'login' %}
requirelogin             {% requireLogin %}
requirepermission        {% requirePermission "spendTheNight" %}
switch                   {% switch variable %}...{% endswitch %}

csrf                     {{ csrfInput() }}
endbody                  {{ endBody() }}
head                     {{ head() }}

getparam                 craft.app.request.getParam()
getbodyparam             craft.app.request.getBodyParam()
getqueryparam            craft.app.request.getQueryParam()
getsegment               craft.app.request.getSegment()

case                     {% case "value" %}
endcache                 {% endcache %}
endifchildren            {% endifchildren %}
endcss                   {% endcss %}
endjs                    {% endjs %}
endnav                   {% endnav %}

ceil                     ceil()
floor                    floor()
max                      max()
min                      min()
shuffle                  shuffle()
random                   random()
round                    num | round()
url, urla                url('path'), url('path', params, 'http', false)

rss                      Example rss feed

dd                       <pre>{{ dump() }}</pre>{% exit %}
dump                     <pre>{{ dump() }}</pre>
```

### Example Forms

```bubble

formlogin                Example login form
formuserprofile          Example user profile form
formuserregistration     Example user registration form
formforgotpassword       Example forgot password form
formsetpassword          Example set password form
formsearch               Example search form
formsearchresults        Example search form results

```

### Reference Hints

```bubble

info            All craft.assets properties and template tags
info            All craft.crategories properties and template tags
info            All craft.config properties and template tags
info            All craft.entries properties and template tags
info            All craft.feeds properties and template tags
info            All craft.fields properties and template tags
info            All craft.globals properties and template tags
info            All craft.request properties and template tags
info            All craft.sections properties and template tags
info            All craft.session properties and template tags
info            All craft.tags properties and template tags
info            All craft.users properties and template tags
info            All craft globals (site info, date, users, template tags)

```

## Author

👤 **Ahmed Mohamed Ibrahim**

* Github: [@DinoPHP](https://github.com/DinoPHP)

## 🤝 Contributing

Contributions, issues and feature requests are welcome !<br />Feel free to check [issues page](https://github.com/DinoPHP/BubbleTemplateEngine/issues).

## Show your support

Give a ⭐️ if this project helped you !