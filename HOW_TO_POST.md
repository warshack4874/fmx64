# How to post an update

1. On GitHub, open the `fmx64` repository, go into the `_posts` folder and press **Add file → Create new file**.
2. Name it `YYYY-MM-DD-short-title.md`, for example `2026-12-01-faster-graphics.md`. The date in the name is the post's date.
3. Start it with this header, then write the post in Markdown below it:

   ```
   ---
   layout: post
   title: "Faster graphics"
   image: assets/img/some-screenshot.jpg
   ---

   The first paragraph is shown as the summary on the Updates page.

   ## A heading

   - a list item
   ```

   `image` is optional; it is the picture shown when the link is shared (Discord, etc.).
4. Press **Commit changes**. The site updates in about a minute.

To add pictures, upload them into `assets/img` first (**Add file → Upload files**) and use them in a post with:

```
![What the picture shows]({{ site.baseurl }}/assets/img/your-picture.jpg)
```

# How to release a new launcher version

1. Build the release archive on the PC with `tools\package_release.ps1` (it checks that no game files are inside).
2. On GitHub, open **Releases → Draft a new release**, create a tag such as `v0.2.0`, attach the zip, write the changes, and publish.
3. The site's Download button always points to the latest release, so it needs no change.
4. Optionally post about it in `_posts` as above.
