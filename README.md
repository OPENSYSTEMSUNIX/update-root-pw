# update-root-pw

## playbook layout
`
- hosts: all
  tasks:
  - name: Change root password
    user: 
      name=root 
      update_password=always 
      password="$6$rounds=656000$Il.7J6fa8icfJBRy$DfkyR/9w/KTBXIeRCNl.816BpJZ/6cw3xmRTpn3NeXjoTzogDCW7kvJhP66IJU/GulqmfsLNAklK2uvgqVpMK/"
`

## Variables
`password=`    #hash of password

## how to generate passwords

`# sudo pip install passlib`
`# python -c "from passlib.hash import sha512_crypt; import getpass; print sha512_crypt.encrypt(getpass.getpass())"`
Enter the password whe  prompted. The output will be the hash to use for the password varible.
