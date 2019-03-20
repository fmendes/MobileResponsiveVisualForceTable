# MobileResponsiveVisualForceTable
# An easier way to make VisualForce tables mobile friendly

(Code to add to VisualForce tables in order to make them resize and rearrange elements according to a mobile device screen size)

The default behavior of VisualForce tables (apex:pageBlockTable and apex:dataTable) is static - they don't rearrange the data to better fit tablets and smartphones.

For that reason, I've implemented a CSS solution based on principles described on [this article at CSS-tricks.com](https://css-tricks.com/responsive-data-tables/) and have added several adjustments to make it work requiring minimal changes to the VisualForce code.

This solution resizes and rearranges the table data according to the screen size and can be implemented in 3 steps:

1. use the "mobileFriendly.css" file above - it contains the CSS directives to make a browser respond to the screen size

2. add to your apex:pageBlockTable or apex:dataTable the attribute below:
```
styleClass="mobileFriendly"
```
3. for each column in your table, add the attribute below containing the column header to display
```
html-data-header="your column header text"
```

The result is below (animated GIF showing the table responding to screen resizing):

![alt text](http://url/to/img.png)



