
└─[$]> bash /home/sticks/.encrypt_envrc.sh
Bundling .envrc files...
Encrypting archive...
enter AES-256-CBC encryption password:
Verifying - enter AES-256-CBC encryption password:

Created: /home/sticks/bin/envrc-backup.tar.gz.enc

To restore on another machine:
  openssl enc -d -aes-256-cbc -pbkdf2 -in envrc-backup.tar.gz.enc -out envrc-backup.tar.gz
  tar -xzf envrc-backup.tar.gz -C $HOME
