Lorem Ipsum Master Detail
===

## Code Wars Challenge

Complete [today's Kata.](https://www.codewars.com/kata/my-head-is-at-the-wrong-end)

## Lab

Create a ipsum viewer/editor that:

* Displays a lists of ipsum's and when an ipsum is clicked, it populates a detail view with full information.
* The Detail has an edit button that toggles to a form and allows editing. Includes sample text in html
* Add an input form and button for a title that adds a new ipsum and makes it the selected item. 

(BONUS: Can you get the detail to switch to edit mode?)

## Components

Your app components should be structured as follows:

```
App
  Header
  Ipsums
    AddIpsum
    IpsumList
        IpsumItem
    Ipsum
        IpsumDetail
        IpsumForm
```

## Component Details

* `App` 
    * Top Level Component
* `Header`
    * Logo and Title
* `Ipsums`
    * owns the "ipsum list" state (data, use your `ipsumApi` service)
        * adds and updates **need to be done in this component**!
    * owns the "selected" state (initially `null`)
    * passes `IpsumList` list of `ipsums` and a callback function, `onSelect`
    * passes `AddIpsum` a callback function `onAdd`
    * passes `Ipsum` the `ipsum` (it's `selected` data) and an `onUpdate` callback
* `IpsumList`
    * calls the passed `onSelect` when an ipsum is selected, _passing the corresponding object_ to the `onSelect` function
    * show name and category
* `IpsumForm`
    * Form for creating or updating an `ipsum`
    * gets passed an `onUpdate` callback called for add and edit when form submitted
    * gets passed the `ipsum` if updating
    * Has own state for managing data being updated (copy in data function when editing)
    * Only show "cancel" button when updating. Calls `onCancel` when cancel button clicked
* `Ipsum`
    * Container for switching between viewer and editor (form)
    * Has "editing" state (data)
    * If `ipsum` is `null` displays message to make a selection
    * Passes IpsumDetail the `ipsum` for display
    * Passes IpsumForm the `ipsum` to edit, a `onCancel` callback function, and the `onUpdate` from `Ipsums`
* `IpsumDetail`
    * gets passed the `ipsum`

## Commits

Work through the tasks incrementally:

1. Design List
1. Implement List
1. Design Detail View
1. Implement Detail View and Wire to Selected
1. Design Form for Adding
1. Implement Form for Adding and Wire to push into data
1. Add Toggle to Detail View to Show Form
1. Modify Form to Handle Edits (and Cancels)

## Build

Include `npm` `test` script that runs `npm run lint`
    
## Rubric

* Follows prescribed project and component structure and organization **1pt**
* Ipsum list **1pt**
* Shows selected detail view **2pts**
* Switch edit/view modes (including cancel and post-update) **1pt**
* Edit Form **1pt**
* Updates Ipsum **1pt**
* Add Ipsum **1pt**
* Integration: Feature/Functionality correct/works **2pts**
