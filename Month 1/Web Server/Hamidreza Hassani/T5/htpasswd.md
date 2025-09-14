# How to work with htpasswd command?

the `htpasswd` command in in the apache2-util package.

to create a new file that contains username and password, we can run this command

```bash
# -c: creates a new file
# -B: this uses Bcrypt algorithm to hash the password, which is way more secure than the default algorithm (MD5)
# admin is the username that we want to add
sudo htpasswd -B -c /etc/nginx/.htpasswd admin
```
after running this command the program asks you to input the password and then you are good to go.

to add other users simply run this command:
```bash
sudo htpasswd -B /etc/nginx/.htpasswd dev
```