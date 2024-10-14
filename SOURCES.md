
```bash
REVISION=02b8adc
wget -q -O - https://raw.githubusercontent.com/lipis/flag-icons/$REVISION/css/flag-icons.css | sed -r 's#../flags#../img/imedge/vendor/flags#g' > public/css/flag-icons.less
rm -rf public/img/flags
git clone https://github.com/lipis/flag-icons flag-icons
git --work-tree flag-icons --git-dir flag-icons/.git reset --hard $REVISION
cp -r flag-icons/flags public/img/
rm -rf flag-icons
```
