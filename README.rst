=========================
django-object-permissions
=========================

Object granular permissions for Django.

Configuration
==============

In order to use django-object-permissions you must add 
the following to your django settings:

    * `Add 'objperms' to INSTALLED_APPS`
    * `Add 'objperms.backend.ObjectPermBackend' to AUTHENTICATION_BACKENDS`


Usage
=====

Add a permission::

    from objperms.models import ObjectPermission

    ObjectPermission.objects.create(user=user, content_object=my_object,
        view=True, change=False, delete=False)

Checking for permissions::

    if request.user.has_perm('view', my_object):
            """ do something """
