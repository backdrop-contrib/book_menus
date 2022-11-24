# Book Menus
Book Menus allows you to set books as normal Backdrop CMS menus. This means
they will be listed in admin/structure/menu, and have all of the additional
functionality that comes along with it.

This will allow you to use menu manipulation modules. For example, the initial
development was due to wanting a more flexible book menu structure with titles
or sections that are not necessarily links. This can be done using Book Menus
along with [Special Menu Items](https://github.com/backdrop-contrib/special_menu_items).

## Requirements
This module requires that the following modules are also enabled:

- Book - part of Core, disabled by default.
- Menu - part of Core, enabled by default.

## Installation
- Install this module using the official Backdrop CMS instructions at
  https://docs.backdropcms.org/documentation/extend-with-modules.

- To manage the menu, the user must have the `administer menus` permission in
addition to the book permissions.

## Configuration
- Create some books.
- Navigate to `admin/content/book/settings` and chose the Book Menus.
- On the book list page, the edit operation will redirect to the normal menu.
- You can also see the menu at `admin/structure/menu`.
- Modify the menu as required.

### Blocks

This menu provides a block, *Book Menu Navigation*, that is similar in
functionality to core `book.module` with the *show block only on book pages*
setting.

However, the main difference it that it will always show the full tree.  This
was necessary as non-book menu links and #below items weren't getting rendered
as core book.module passes the book menu item to menu_tree_output.

You can still use the core `book.module` Book Navigation block, but on Book Menus
it will likely be the *Book Menus Navigation* block you're looking for.

### Notes
- As this module intercepts the `admin/content/book/*` page, other book
  manipulation module may not work with it.

## Issues
Bugs and Feature Requests should be reported in the Issue Queue:
https://github.com/backdrop-contrib/book_menus/issues.

## Current Maintainers
- [Martin Price](https://github.com/yorkshire-pudding) - [System Horizons Ltd](https://www.systemhorizons.co.uk)

## Credits

- Ported to Backdrop CMS by [Martin Price](https://github.com/yorkshire-pudding) - [System Horizons Ltd](https://www.systemhorizons.co.uk)
- Created for Drupal by [Sam K Hall](https://github.com/skh-)

## License


This project is GPL v2 software.
See the LICENSE.txt file in this directory for complete text.
