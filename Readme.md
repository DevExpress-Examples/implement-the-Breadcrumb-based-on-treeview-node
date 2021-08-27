<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/230153384/20.2.5%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T848395)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Index.razor](./CS/TreeViewBreadcrumbs/Pages/Index.razor)
<!-- default file list end -->

### TreeView for Blazor - How to implement the Breadcrumb control based on a selected node

This example uses the  [Bootstrap Breadcrumb](https://getbootstrap.com/docs/4.0/components/breadcrumb/) component that is bound to DxTreeView via the [SelectionChanged](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxTreeView.SelectionChanged) event handler. TreeView's selected node is changed when a Breadcrumb item is selected:
```
<a @onclick="@(() => SelectNode(currentNodeInfo.Text))" href="#">
    @currentNodeInfo.Text
</a>

...

void SelectNode(string text) {
    TreeView.SelectNode((n) => n.Text == text);
}
```
![](/TreeView.png)
