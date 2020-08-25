# MainMenu

Introducing the Spheroid UI Engine, we need to focus on one of 
its two major components, a MainMenu. 

Along with [Page](page.md), 
MainMenu is a class you need to use in your app to build any UI.
Unlike Page, which you use in order to build UI in non-AR space, 
you use MainMenu to place different UI-elements,
like buttons, icons, texts, etc. atop of AR. 

You can find a quickstart with all source code you need to try the examples 
[here](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/UI).

## Basics

This example creates a MainMenu consisting of one icon placed inside a container,
and upon clicking this icon the page opens:

```
MainMenu {
     Container(top = 20dp, left = 20dp) {
         Image(source = Source("/assets/menu.png"), width = 40dp).onClick {
             mainPage().navigate()
         }
     }
 }
```

## Related Links

- [MainMenu class reference](../reference/spheroid.client.ui/-main-menu/index.md)
- [Full list of UI components](index.md)
- [UI Demo App](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/UI)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)