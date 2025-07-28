---
description: >-
  Search is a special type of input field that is used for processing a query
  and presenting the results of the query to the user.
---

# Search Bar

## Best practices

### Layout

* Don't build a custom search control based on the default text box or any other control.
* Use a search box without a parent container when it's not restricted to a certain width to accommodate other content. This search box will span the entire width of the space it's in.

### Content

* Use placeholder text in the search box to describe what people can search for. For example, "Search", "Search files", or "Search contacts list".
* The search toolkit allows the users to search across different scopes as described below
  * **Global**: Searches across multiple sources of apps, cloud and local content. This is supported by deep search where results are obtained from within different applications in context to those applications and presented for instant action.
  * **Local:** Search within the current application scope.
  * **Web**: Search a web index. Results include pages, entities, and answers.

## Search Bar

### States

![](<../../.gitbook/assets/image (13).png>)

### Transitions

| **Transitions** | **Front View**                                                                    | **Isometric View**                                                                |
| --------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **Appear**      | <p></p><p><img src="../../.gitbook/assets/Search_Appear_Front.gif" alt=""></p>    | <p></p><p><img src="../../.gitbook/assets/Search_Disappear_Persp.gif" alt=""></p> |
| **Enter**       | <p></p><p><img src="../../.gitbook/assets/Search_Enter_Front.gif" alt=""></p>     | <p></p><p><img src="../../.gitbook/assets/Search_Enter_Persp.gif" alt=""></p>     |
| **Exit**        | <p></p><p><img src="../../.gitbook/assets/Search_Exit_Front.gif" alt=""></p>      | <p></p><p><img src="../../.gitbook/assets/Search_Exit_Persp.gif" alt=""></p>      |
| **Interact**    | <p></p><p><img src="../../.gitbook/assets/Search_Interact_Front.gif" alt=""></p>  | <p></p><p><img src="../../.gitbook/assets/Search_Interact_Persp.gif" alt=""></p>  |
| **Disappear**   | <p></p><p><img src="../../.gitbook/assets/Search_Disappear_Front.gif" alt=""></p> | <p></p><p><img src="../../.gitbook/assets/Search_Disappear_Persp.gif" alt=""></p> |
