Notes

Today I learned how Linux controls access using users, groups, and permissions.

Key concepts:

* Users → Individual accounts
* Groups → Collection of users
* Root → Full system access

Permissions:

* r = read
* w = write
* x = execute

Numeric values:

* 7 = rwx
* 6 = rw-
* 5 = r-x
* 4 = r–

Commands:

* whoami → Show current user
* groups → Show user groups
* ls -l → View permissions
* chmod → Change permissions
* chown → Change ownership

Principle of Least Privilege:
Users should only have the minimum access required.
