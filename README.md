# ASP .NET Core MVC Grid Tag Helper

## Introduction

Grid tag helper represents a powerful Datagrid UI tag helper. It offers rich functionality, easy to use APIs and works across devices and browsers. The grid component delivers advanced data visualization features and built-in support for server-side paging, editing, sorting and filtering. 

## Highlights

```Works across devices and browsers```
```Web Standards Compliant```
```Rich and easy to use JavaScript API```
```Optimized for Performance```
```Easy customization and built-in themes```
```Localization```
## Features

Data Binding
Outlook-Style Grouping
Sorting
Filtering
Paging
Editing and Validation
Nested Grids
Row Details
Localization
Column Types
Columns Resizing
Columns Reorder
Columns Hierarchy
Pinned Columns
Foreign Columns
Cells Formatting
Custom Cells Rendering
Custom Cell Editors
Rows and Cells Selection
Aggregates
Export to Excel, XML, HTML, CSV, TSV, PDF and JSON
Printing
Keyboard Navigation
State Maitenance

Tag Helper enables server-side code to participate in creating and rendering HTML elements in Razor files.

## Grid Demos

[ASP .NET Core MVC Tag Helpers Demos page](http://www.jqwidgets.com/asp.net-core-mvc-tag-helpers/asp.net-core-mvc-grid-tag-helper/index.htm).

## Setup

### 1. Create a new ASP .NET Core Web Application
![alt text](http://aspcore.jqwidgets.com/bootstrap/tag-helpers/images/aspnetcore-net-project.png "Tag Helpers 1")

![alt text](http://aspcore.jqwidgets.com/bootstrap/tag-helpers/images/aspnetcore-webapplication.png "Tag Helpers 2")

### 2. Reference the Tag Helpers

Install the Tag Helper's Nuget package from https://www.nuget.org/packages/jQWidgets.AspNetCore.Mvc.TagHelpers/1.0.0.
### 3. Update _ViewImports.cshtml

```
@using jQWidgets.AspNetCore.Mvc.TagHelpers
@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers
@addTagHelper *, jQWidgets.AspNetCore.Mvc.TagHelpers
@inject Microsoft.ApplicationInsights.Extensibility.TelemetryConfiguration TelemetryConfiguration
```

### 4. Build the Solution

Click Build in the top menu bar of Visual Studio, then click Build Solution to Build the solution


### 5. Add a Tag Helper to a Page

We can now add a Tag Helper to one of the views (pages).
For example, we will add the Tag Helper to Views\Home\About.cshtml.
While typing, IntelliSense suggest the existing Tag Helpers:

```html
@model IEnumerable<jQWidgets.AspNet.Core.Models.Employee>
@{
    ViewData["Title"] = "ASP .NET MVC Grid Example";
}
<script src="~/jqwidgets/jqxbuttons.js"></script>
<script src="~/jqwidgets/jqxscrollbar.js"></script>
<script src="~/jqwidgets/jqxgrid.js"></script>
<script src="~/jqwidgets/jqxgrid.edit.js"></script>
<script src="~/jqwidgets/jqxgrid.columns-resize.js"></script>
<script src="~/jqwidgets/jqxgrid.filter.js"></script>
<script src="~/jqwidgets/jqxgrid.selection.js"></script>
<script src="~/jqwidgets/jqxgrid.sort.js"></script>
<script src="~/jqwidgets/jqxgrid.pager.js"></script>
<script src="~/jqwidgets/jqxgrid.aggregates.js"></script>
<script src="~/jqwidgets/jqxgrid.grouping.js"></script>
<script src="~/jqwidgets/jqxmenu.js"></script>
<script src="~/jqwidgets/jqxlistbox.js"></script>
<script src="~/jqwidgets/jqxdropdownlist.js"></script>

@model IEnumerable<jQWidgets.AspNet.Core.Models.Employee>

@{
    ViewData["Title"] = "ASP .NET MVC Grid Example";
}

<jqx-grid theme="@ViewData["Theme"]" sortable="true" filterable="true" auto-height="true" width="850" source="Model"> 
    <jqx-grid-columns>
        <jqx-grid-column column-group="name" datafield="FirstName" width="100" text="First Name"></jqx-grid-column>
        <jqx-grid-column column-group="name" datafield="LastName" width="100" text="Last Name"></jqx-grid-column>
        <jqx-grid-column datafield="Title" width="150"></jqx-grid-column>
        <jqx-grid-column datafield="Address" width="200"></jqx-grid-column> 
        <jqx-grid-column datafield="City" width="150"></jqx-grid-column>
        <jqx-grid-column datafield="Country"></jqx-grid-column>
  </jqx-grid-columns>
    <jqx-grid-column-groups>
        <jqx-grid-column-group name="name" text="Name"></jqx-grid-column-group>
    </jqx-grid-column-groups>
</jqx-grid>


```
