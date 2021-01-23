# Security

* [x] Remove insecure [MD5 hash function]
* [x] Implement modern encryption standards through [bcrypt hashed passwords]
* [x] Isolate `docroot` to limit access to config files, databases, and third party libraries

[MD5 hash function]: https://core.trac.wordpress.org/ticket/21022 "Use bcrypt for password hashing"
[bcrypt hashed passwords]: https://github.com/roots/wp-password-bcrypt "wp-password-bcrypt"
