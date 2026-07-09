How to generate and install PNG icons for Tranzivo

1) Open the generator in a browser:

   - Open file:// path in your browser or serve the folder, e.g.:

     cd c:\aplikasipos
     npx http-server . -p 8080
     # then open http://localhost:8080/tools/export-icons.html

2) Click "Download 192×192 PNG" and "Download 512×512 PNG" (or "Download both").
3) Replace the icons in the project:

   - Copy the downloaded files to `icons/` and `www/icons/`:

     copy icon-192.png icons\icon-192.png
     copy icon-512.png icons\icon-512.png
     copy icon-192.png www\icons\icon-192.png
     copy icon-512.png www\icons\icon-512.png

4) Sync to Android (if using Capacitor):

   cd c:\aplikasipos
   npx cap copy android

Notes
- The generator produces simple rounded-square icons with a white inset and a "T" glyph. If you want different artwork, edit `tools/export-icons.html`.
- For Play Store, use Android Studio to create adaptive icons and a signed AAB.
