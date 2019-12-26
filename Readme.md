<!-- default file list -->
*Files to look at*:

* [Index.razor](./CS/TreeViewBreadcrumbs/Pages/Index.razor)
<!-- default file list end -->

### TreeView for Blazor - How to implement the Breadcrumb control based on a selected node

This example uses the  [Bootstrap Breadcrumb](https://getbootstrap.com/docs/4.0/components/breadcrumb/) component that is bound to DxTreeView via the [SelectionChanged](https://docs.devexpress.com/Blazor/DevExpress.Blazor.Base.DxTreeViewBase.SelectionChanged) event handler. TreeView's selected node is changed when a Breadcrumb item is selected:
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
