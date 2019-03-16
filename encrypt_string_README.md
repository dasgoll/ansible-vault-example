### We want to write author name 'Jameel Jamal' to /tmp/este

echo elpasswordgrande > password_file


ansible-vault encrypt_string --vault-id password_file 'Jameel Jamal' --name 'authorName'



ansible-playbook -i localhost, -c local site2.yml --ask-vault-pass
