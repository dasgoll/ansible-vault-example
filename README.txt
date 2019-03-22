We want to change password of a user called 'khaled' to 'eva2niva'

ansible all -i localhost, -m debug -a "msg={{ 'eva2niva' | password_hash('sha512', 'mysecretsalt') }}"

OR
### apt install whois
mkpasswd --method=sha-512

OR
$ htpasswd -c /tmp/my_hash user1
New password: 
Re-type new password: 
Adding password for user user1
$ cat /tmp/my_hash
user1:$6$mysecretsalt$Rfl3Gk82uFh6nAD.edgZB.zf7CcKTdQx2/VWY/2LDSf.fYZJUjAkuF0z3AkYp9JVRsTI8jvmNzg/QpjfRoVBj/
Obviously, you just grab the 2nd field, and can delete the file once you're added it to shadow or for use with sudo (still most likely shadow).


 
 ### N.B: include_vars can include yaml and json files

 ansible-vault encrypt vault.yml
 # use password 'elpassgrande'
 OR  echo elpasswordgrande > password_file

ansible-playbook -i localhost, -c local site.yml --ask-vault-pass
OR
ansible-playbook -i localhost, -c local site.yml  --vault-password-file password_file

 su - khaled

 
