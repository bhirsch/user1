This module restricts access to user 1 to prevent 
users with limited admin access from hijacking permissions. 

When user1 is enabled, users other than user 1 (uid = 1)
will not be able to edit user 1's password and thereby gain
access to permissions that should be off limits. 

user1 does this by 

1. Excluding user 1 from the admin/user/user listing of users 
   (which has an edit link, enabling people with 'administer
    users' permissions to change users' passwords).

2. Denying anyone other than user 1 access to the 
   path: admin/user/1/edit.

NOTE: If your site has any roles that are able to edit 
permissions or execute PHP, clever users 
can easily work around these restrictions.
