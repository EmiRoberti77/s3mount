## S3 mounting

install AWS cli

```bash
brew install awscli
```

add AWS credentials

```bash
aws configure
```

install mac FUSE to manage the filesystem extentions

```bash
brew install macfuse
```

download rclone to manage mount

```bash
curl -O https://downloads.rclone.org/rclone-current-osx-amd64.zip
```

unzip the package

```bash
unzip rclone-current-osx-amd64.zip
```

move to bin

```bash
sudo mv rclone /usr/local/bin/
```

start config

```bash
rclone config
```

## Choose n to create a new remote.

-     Name the remote (e.g., s3remote).
-     Select 4 for Amazon S3.
-     Enter your AWS Access Key ID and Secret Key.
-     Choose your region (e.g., us-east-1).
-     Leave the rest as default or adjust as necessary.

create mount dir

```bash
mkdir s3mount
```

mount drive to s3

```bash
rclone mount s3remote:emibucketai /Users/user/s3mount --vfs-cache-mode writes
```

on a mac M series the mount will fail. follow these steps to change file system settings

- https://github.com/macfuse/macfuse/wiki/Getting-Started
