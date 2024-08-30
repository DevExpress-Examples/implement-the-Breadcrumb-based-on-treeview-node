<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/230153384/24.2.1%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T848395)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->

# TreeView for Blazor - How to implement the Breadcrumb control based on a selected node 

The Breadcrumb control indicates the current page's location in a navigational hierarchy:

![TreeView as Breadcrumb](/TreeView.png)

In this example, the DxTreeView component uses its [SelectionChanged](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxTreeView.SelectionChanged) event handler to bind to the [Bootstrap Breadcrumb](https://getbootstrap.com/docs/4.0/components/breadcrumb/) component.

The TreeView's selected node changes when you select a Breadcrumb item:
```
<a @onclick="@(() => SelectNode(currentNodeInfo.Text))" href="#">
    @currentNodeInfo.Text
</a>

@* ... *@

void SelectNode(string text) {
    TreeView.SelectNode((n) => n.Text == text);
}
```

<!-- default file list -->
## Files to Look At

[Index.razor](./CS/TreeViewBreadcrumbs/Pages/Index.razor)
<!-- default file list end -->

## Documentation

[TreeView - SelectionChanged](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxTreeView.SelectionChanged)
<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=implement-the-Breadcrumb-based-on-treeview-node&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=implement-the-Breadcrumb-based-on-treeview-node&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
