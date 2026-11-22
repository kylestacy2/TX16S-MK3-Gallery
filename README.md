# KSE Image Gallery for the TX16S MK3

[Open the gallery](https://kylestacy2.github.io/TX16S-MK3-Gallery/)

Select an image to preview it on the 800 × 480 KSE Touch dashboard in Transparent mode. Try different model and wallpaper combinations using the selector below the screen. Splash screens also have an **At startup** view. The preview uses the electric dashboard layout with sample telemetry.

| Collection | Files to copy onto the radio |
| --- | --- |
| [Model images](model-images/) | Full-size aircraft PNGs in `/IMAGES/`. Match the filename to the aircraft name for KSE Touch's automatic lookup. |
| [Wallpapers](wallpapers/) | 800 × 480 backgrounds in `/IMAGES/Wallpapers/`. Choose **Appearance → Wallpaper & Startup** and apply the background. |
| [Startup screens](startup-screens/) | 800 × 480 splash screens in `/IMAGES/Wallpapers/`. Choose and apply the startup image on the same settings page. |

Use **Download PNG** on a card or preview page to save one image. Each collection has a ZIP. **Download all images** includes all three collections. Unzip a pack and merge its `IMAGES` folder into your SD card. The model pack preserves full-size originals and their filenames. A compact 192 × 114 thumbnail with a short filename is available on each model's preview page for the EdgeTX model picker.

For transparent tiles on the radio, set **Dashboard → Options → Dashboard theme** to **Transparent** and turn off shared theme matching. For a standard EdgeTX theme, save a copy of its current background and place your chosen wallpaper in the theme folder as `background_800x480.png`.

[KSE Touch guide](https://github.com/kylestacy2/KSE-Touch#appearance) · [EdgeTX theme files](https://github.com/EdgeTX/themes/blob/main/structure.md) · [EdgeTX model images](https://manual.edgetx.org/color-radios/radio-settings/storage)

## Add artwork

Put a PNG directly in `model-images/`, `wallpapers/` or `startup-screens/`. Wallpapers and splash screens use 800 × 480. Keep the model PNG at its original dimensions with its original transparency. To supply a display title or a short EdgeTX thumbnail filename, add a row to `catalog.csv`. Otherwise the gallery uses the filename to generate them.

## Preview locally

Install Pillow with `python3 -m pip install -r requirements.txt`, run `python3 build_gallery.py`, then open `_site/index.html` in a browser. The preview and downloads work offline. The packaged gallery also includes a ready-to-open `index.html` in its top folder.

## Publish on GitHub Pages

In **Settings → Pages → Build and deployment**, select **GitHub Actions** as the source. Push to `main` or run **Actions → Publish gallery → Run workflow**. The workflow rebuilds the gallery, per-image previews and ZIP packs whenever new artwork is pushed.
