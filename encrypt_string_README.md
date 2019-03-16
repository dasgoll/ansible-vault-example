echo elpasswordgrande > password_file

We want to write author name 'Jameel Jamal' to /tmp/este


ansible-vault encrypt_string --vault-id password_file 'authorName' --name 'string_name'



ansible-playbook -i localhost, -c local site2.yml --ask-vault-pass