# Columns Plugin

This is a plugin for [Kirby](http://getkirby.com/) enables a simple syntax in Kirbytext for multi-column layouts/text.

## Installation

Put the `columns` folder in `/site/plugins`.

## Example usage in Kirbytext

```
(columns…)

## Column A
In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium. Integer tincidunt. Cras dapibus. Vivamus elementum semper nisi. Aenean vulputate eleifend tellus. Aenean leo ligula, porttitor eu, consequat vitae, eleifend ac, enim. Aliquam lorem ante, dapibus in, viverra quis, feugiat a.

++++

## Column B
In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium. Integer tincidunt. Cras dapibus. Vivamus elementum semper nisi. Aenean vulputate eleifend tellus. Aenean leo ligula, porttitor eu, consequat vitae, eleifend ac, enim. Aliquam lorem ante, dapibus in, viverra quis, feugiat a.

++++

## Column C
In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium. Integer tincidunt. Cras dapibus. Vivamus elementum semper nisi. Aenean vulputate eleifend tellus. Aenean leo ligula, porttitor eu, consequat vitae, eleifend ac, enim. Aliquam lorem ante, dapibus in, viverra quis, feugiat a.

(…columns)

## Example CSS

Add the following rules to your CSS to enable the column layout:

```css

.columns {
  margin-right: -2rem;
}
.column {
  display: inline-block;
  vertical-align: top;
  padding-right: 2rem;
}
.columns-1 .column {
  width: 100%;
}
.columns-2 .column {
  width: 50%;
}
.columns-3 .column {
  width: 33.33%;
}
.columns-4 .column {
  width: 25%;
}
.columns-5 .column {
  width: 20%;
}

``

Modify the gutter between columns by changing the right margin on the .columns container and the right padding on the .column

## Modifying class names

Class names for the container and the column divs can be modified in your config:

```php

c::set('columns.container', 'mycolumns');
c::set('columns.item', 'mycolumn');

```