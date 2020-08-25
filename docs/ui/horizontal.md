# Horizontal

On this page, we focus on one of the basic components of Spheroid UI Engine, a Horizontal.
You can find a quickstart with all source code you need to try the examples 
[here](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/UI).

As well as a [Vertical](vertical.md), a Horizontal
serves to organize nested elements, the elements of one kind (buttons, images, etc.)
as well as elements of different kinds (an image and a text, and so on).

Every element nested inside a Horizontal must be wrapped in a 
[Container](container.md).

Below, you will find the examples of using the Horizontal class.
The images corresponding to each example illustrate how the horizontal will look 
on the mobile device when using different settings.

## Default settings

This is how the buttons nested inside a horizontal will look with the default settings: 

```
Horizontal {
    Container {
        Button(text = "Item 1")
    }
    Container {
        Button(text = "Item 2")
    }
    Container {
        Button(text = "Item 3")
    }
}
```

![](../images/ui/horizontal/horizontal-default.png)

## Visibility

A horizontal is visible by default.
However, there are cases when you need to turn the visibility on and off. 
You do this by setting the `isVisible` property value `true` or `false`. If you set `false`,
all elements nested inside a horizontal will become invisible too.

## Spacing

If you need to change the distance between the elements nested inside a horizontal,
set the value of a `spacing` property:

```
Horizontal(spacing = 2dp) {
    Container {
        Button(text = "Item 1")
    }
    Container {
        Button(text = "Item 2")
    }
    Container {
        Button(text = "Item 3")
    }
}
```

![](../images/ui/horizontal/horizontal-spacing.png)

## Horizontal and vertical alignment

Sometimes, you need to change the relative position of a horizontal to the external container.
You have a set of properties to do this. Note that by default the container is transparent, 
so we have used a [Color](../reference/spheroid.client.ui/-color/index.md) 
class instance in the examples.

The `horizontalAlign` property sets the horizontal alignment of the horizontal
to left, right or center:

```
Container(backgroundColor = Color(rgb = 0xEEEEEE)) {
    Horizontal(horizontalAlign = "center") {
        Container {
            Button(text = "Item 1")
        }
        Container {
            Button(text = "Item 2")
        }
    }
}
```

![](../images/ui/horizontal/horizontal-horizontal-alignment.png)

The `left` and `right` properties allow you to place the horizontal 
at an exact distance from the left or the right border of the external container:

```
Container(backgroundColor = Color(rgb = 0xEEEEEE)) {
    Horizontal(left = 12dp) {
        Container {
            Button(text = "Item 1")
        }
        Container {
            Button(text = "Item 2")
        }
    }
}
```

![](../images/ui/horizontal/horizontal-left.png)

The `verticalAlign` property sets the vertical alignment of the horizontal
to top, bottom or center:

```
Container(backgroundColor = Color(rgb = 0xEEEEEE), height = 90dp) {
    Horizontal(verticalAlign = "center") {
        Container {
            Button(text = "Item 1")
        }
        Container {
            Button(text = "Item 2")
        }
    }
}
```

![](../images/ui/horizontal/horizontal-vertical-alignment.png)

Using the `top` and `bottom` properties, you can customize 
the distance between the horizontal and the top or the bottom border of the external container:

```
Container(backgroundColor = Color(rgb = 0xEEEEEE), height = 90dp) {
    Horizontal(bottom = 8dp) {
        Container {
            Button(text = "Item 1")
        }
        Container {
            Button(text = "Item 2")
        }
    }
}
```

![](../images/ui/horizontal/horizontal-bottom.png)

## Related Links

- [Horizontal class reference](../reference/spheroid.client.ui/-horizontal/index.md)
- [Full list of UI components](index.md)
- [UI Demo App](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/UI)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)