grub2-themes-ubuntu-mate
========================

![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)
grub2-themes-ubuntu-mate by Ivan Pejić aka nadrimajstor is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)

* PNGs and theme.txt files goes to `/boot/grub/themes/ubuntu-mate`
* a tiny patch to `/lib/plymouth/themes/default.grub`

```diff
@@ -1,3 +1,10 @@
-if background_color 44,0,30; then
+if background_color 60,59,55; then
   clear
 fi
+
+color_normal=light-gray/black
+
+if [ -e /boot/grub/themes/ubuntu-mate/theme.txt ]; then
+  insmod png
+  theme=/boot/grub/themes/ubuntu-mate/theme.txt
+fi
```
And the final result should look like:

![final](docs/final.ong)
