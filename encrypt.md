zip -r MySecretFolder.zip MySecretFolder

openssl enc -aes-256-cbc -salt -in MySecretFolder.zip -out MySecretFolder.zip.enc
openssl enc -d -aes-256-cbc -in MySecretFolder.zip.enc -out MySecretFolder.zip
