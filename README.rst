===========
django-object-permissions
===========

Object granular permissions for Django.

Configuration.
=========================================

In order to use django-object-permissions you must add 
the following to your django settings:

    * `Add 'objperms' to INSTALLED_APPS`
    * `Add 'objperms.backend.ObjectPermBackend' to AUTHENTICATION_BACKENDS`


Usage.
=========================================

Add a permission:::
    ObjectPermission.objects.create(user=user, content_object=my_object)

Checking for permissions:::
    if request.user.has_perm('view', account):
        """ do something """
