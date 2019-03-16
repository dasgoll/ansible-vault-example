### We want to write author name 'Jameel Jamal' to /tmp/este

echo elpasswordgrande > password_file


ansible-vault encrypt_string --vault-id password_file 'Jameel Jamal' --name 'authorName'
### take about of above command and update site2.yml


ansible-playbook -i localhost, -c local site2.yml --ask-vault-pass
OR to not prompt for pass
ansible-playbook -i localhost, -c local site2.yml --vault-password-file password_file

cat /tmp/este

