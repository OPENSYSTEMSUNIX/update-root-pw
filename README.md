# update-root-pw

Update the root password with the supplied value.

> Variables
- `password=`       #hash of password
- `name=`           #default root
- `update_password` #default always -- update the password everytime the playbook is run

> how to generate passwords

`# sudo pip install passlib` <br>
`# python -c "from passlib.hash import sha512_crypt; import getpass; print sha512_crypt.encrypt(getpass.getpass())"` <br><br>
Enter the password whe  prompted. The output will be the hash to use for the password varible.
