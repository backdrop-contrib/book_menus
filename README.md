### Introduction ###

Book Menus allows you to set books as normal drupal menus.  This means they will
be listed in `admin/structure/menu`, and have all of the additional
functionality that comes along with it.

This will allow you to use menu-manipulation modules.  For example, the initial
development was due to wanting a more flexible book menu structure with
titles/sections that are not necessairly links.  This can be done using
book_menus along with [special_menu_items][special_menu_items].

Another possibility would be to use it with [menu_html][menu_html].  Say you
have icons requiring special markup like `<span class="icon-book"></span>`.
Book menus will allow you to do this since it's a normal menu.

### Installation ###

- [Enable][enable] as usual,
- To manage the menu, the user must have the `administer menus` permission,
  in addition to the normal book permissions.

### Configuration ###

- Create some books,
- Navigate to `admin/content/book/settings` and chose the Book Menus,
- On the book list page, the edit operation will redirect to the normal menu,
- You can also see the menu ad `admin/structure/menu`,
- Modify the menu as required,
- You can use the original book block to display the menu, or the one that is
  created by default by the core menu module.  Therefore, you can optionally
  integrate it with menu modules such as [nice_menus][nice_menus].

#### Notes ####

- As this module intercepts the `admin/content/book/*` page, other book
  manipulation module may not work with it,
- If you are going to use the standard *Book Navigation* block with the *show
  block only on book pages* setting, ensure that you nest all of the items under
  the book parent, as book.module removes the top-level menu link.  If you would
  like to include the main book page in the menu, just create a new link to the
  book parent in the menu configuration and nest it under the original.

[special_menu_items]: https://www.drupal.org/project/special_menu_items
[menu_html]: https://www.drupal.org/project/menu_html
[enable]: https://drupal.org/documentation/install/modules-themes/modules-7.
[nice_menus]: https://www.drupal.org/project/nice_menus
