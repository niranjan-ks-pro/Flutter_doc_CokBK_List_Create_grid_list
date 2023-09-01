# Flutter_doc_CokBK_List_Create_grid_list
 https://docs.flutter.dev/cookbook/lists/grid-lists
Create a grid list
==================

1.  [Cookbook](https://docs.flutter.dev/cookbook)
2.  [Lists](https://docs.flutter.dev/cookbook/lists)
3.  [Create a grid list](https://docs.flutter.dev/cookbook/lists/grid-lists)

In some cases, you might want to display your items as a grid rather than a normal list of items that come one after the next. For this task, use the [`GridView`](https://api.flutter.dev/flutter/widgets/GridView-class.html) widget.

The simplest way to get started using grids is by using the [`GridView.count()`](https://api.flutter.dev/flutter/widgets/GridView/GridView.count.html) constructor, because it allows you to specify how many rows or columns you'd like.

To visualize how `GridView` works, generate a list of 100 widgets that display their index in the list.

content_copy

```
GridView.count(
  // Create a grid with 2 columns. If you change the scrollDirection to
  // horizontal, this produces 2 rows.
  crossAxisCount: 2,
  // Generate 100 widgets that display their index in the List.
  children: List.generate(100, (index) {
    return Center(
      child: Text(
        'Item $index',
        style: Theme.of(context).textTheme.headlineSmall,
      ),
    );
  }),
),
```

`\
`