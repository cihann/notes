# Django Security

## Access Control / Authorization

  * Permission are implemented per database table. There are three default permissions per model: can_change, can_create, can_delete permissions.

  * Django's has support for per-object (per-row) permissions but the default implementation doesn't use them - this means a third party module could hook into the system to provide logic for per-object permissions.

### restrict URL

  * You can always return a custom response from a view function with an appropriate status code (e.g. 403 or 404).

  * There are builtin decorators for view function to restrict access for a view/url to logged in users, users with a special permi ssion, users who can login into the admin panel, superusers, users that pass a test (test means a function gets a user instance and must return True to grant access).



