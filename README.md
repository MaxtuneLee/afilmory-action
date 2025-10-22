# Deploy Afilmory via Github Action

Deploy your Afilmory site to your server with ease.

## How to use?

Fork the repo, modify `config.json` and `build.config.json` to your configurations.

Add the following env secrets to your repo config:

- `DEPLOY_KEY`: Your SSH private key for deployment.
- `SERVER_ADDRESS`: Your server address.
- `SERVER_USERNAME`: Your server username.
- `SERVER_PORT`: Your server SSH port.
- `S3_ACCESS_KEY_ID`: Your S3 access key ID.
- `S3_SECRET_ACCESS_KEY`: Your S3 secret access key.

Then, trigger the workflow manually from the Actions tab in your GitHub repository.

## Notes

Ensure your server is set up to accept SSH connections using the provided private key.

You can regenerate a new key pair using `ssh-keygen` if needed.

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

then add the public key to your server's `~/.ssh/authorized_keys` file.