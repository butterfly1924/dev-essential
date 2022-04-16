rsync
```bash
watch -n 0 'rsync \
        -avhr \
        -e "ssh -o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null -F /var/folders/yv/xxxxx/T/gitpod_ssh_config" \
        --include="**.gitignore" --exclude="/.git" --filter=":- .gitignore" --delete-after \
        /Volumes/xxxxxxxx/sass-dev sshhostname:/workspace/sass-dev-rsync'
```
