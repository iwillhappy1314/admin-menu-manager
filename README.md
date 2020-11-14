# wp-meta-filter
WordPress Admin Menu Manager

## usage

````php
$menu_manager = new Wenprise\MenuManager\Cleaner();

$menu_manager->remove_menu([
    'edit.php',
    'edit.php?post_type=page',
    'edit.php?post_type=activity',
    'edit.php?post_type=comm',
    'upload.php',
    'themes.php',
    'plugins.php',
    'edit-comments.php',
    'tools.php',
    'options-general.php',
]);

$menu_manager->remove_submenu('index.php', 10)
             ->remove_submenu('themes.php', [6, 15, 20])
             ->remove_submenu('options-general.php', [10, 15, 20, 25, 30, 40]);


if ( ! current_user_can('administrator')) {
    $menu_manager->remove_submenu('edit.php?post_type=staff', [15]);
}
````
