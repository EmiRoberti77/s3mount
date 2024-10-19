- brew install macfuse
- brew install automake autoconf gcc make pkg-config

```bash
git clone https://github.com/s3fs-fuse/s3fs-fuse.git
cd s3fs-fuse
./autogen.sh
./configure --prefix=/usr/local --with-macfuse=/usr/local
make
sudo make install

```

```bash
s3fs emibucketai /Users/emiliano.roberti/S3Mount -o allow_other -o use_cache=/tmp -o nosuid -o rw -o defer_permissions
```

symbolik link

```bash
ln -s /Users/emiliano.roberti/S3Mount/ace.mp4 /Users/emiliano.roberti/Downloads/emi.mp4
```
