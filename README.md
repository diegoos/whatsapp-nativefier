## Create whatsapp application

```sh
nativefier --name "WhatsApp" --icon icon.png --user-agent "safari" --inject wpp-inject.js --browserwindow-options '{ "webPreferences": { "spellcheck": true } }' --verbose --single-instance --tray web.whatsapp.com
```

Once it finishes you will have a new directory in the same location named `whatsapp-linux-x64`, rename this to `whatsapp` and move it to `/opt`.

```sh
mv Whatsapp-linux-x64 whatsapp
sudo mv whatsapp /opt
```

## Update WMClass

To get the `WMClass`:

```sh
xprop WM_CLASS
```

> Place the crosshair on the WhatsApp window. You will get something of the type `whatsapp-nativefier-7bbd2c` in the terminal, change the original value with this in the `whatsapp.desktop` file.

Update the `WMClass` on `whatsapp.desktop` and copy it to `/usr/share/applications`.

```sh
cp whatsapp.desktop /usr/share/applications
```
