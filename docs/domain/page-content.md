# Page content

## Structure

- A page has one layout. Font sizes and the position of every element are fixed by it.
- A page is made of four sections. **Home** is mandatory. **Diary**, **Memories** and **Playlist** are optional; the owner chooses which to include.
- Diary, Memories and Playlist contain items. Items can be placed directly in the section, in a folder, or in a subfolder (maximum depth: section → folder → subfolder → item).
- The owner orders folders and items freely, with one exception: Diary entries are always sorted by their date, **oldest first**, within their container.

### Home

- Couple name (required), a heart, and one text field.
- Optional background image, rendered semi-transparent. It counts as an image.
- Optional relationship day counter. It requires a relationship start date, which cannot be in the future, and shows the number of days since then.

### Diary — entries

- Date (required, cannot be in the future).
- Title, defaulting to the date; the owner may change it.
- Optional image and optional text field.

### Memories — moments

- Title (required).
- Optional image and optional text field.

### Playlist — songs

- Spotify **track** link (required). Album, playlist and artist links are not accepted.
- The song's title and cover are taken from Spotify when the link is added. If Spotify cannot provide them, the song cannot be added.
- Optional text field.
- Visitors see the song with an embedded Spotify player.

## Text

- Text fields support headings, subheadings and body text, with **bold** and _italic_.
- The owner picks one font for headings and one for body text from a curated list.
- **Character counting:** every visible character counts, including spaces, punctuation and line breaks. Formatting does not count. The count covers all text on the page: couple name, folder names, item titles (including song titles) and text fields.

## Images

- Accepted formats: JPEG, PNG, WebP and HEIC. Maximum 10 MB per upload. Animated images are not supported.
- Every image is re-encoded, resized to at most 2048 px on its longest side, and stripped of embedded metadata (such as location).
- Only the number of images matters for limits.

## Colors

- The owner picks a three-color palette: **primary** (headings and clickable elements), **secondary** (subheadings and non-clickable elements) and **tertiary** (background).
- Variations of the tertiary color are generated automatically so that all text meets WCAG AA contrast (4.5:1 for normal text, 3:1 for large text).

## Editor

- Reached at `/edit`. Chrome (not the couple layout): **Publicar**, **Ver página**, **Conta**, and a trial countdown when the page is in Trial.
- Shows images and characters used and remaining (Trial or Paid limits).
- Every field shows a static, non-restrictive placeholder suggesting what to write.
- Prevents adding content beyond a limit.
- Saves the working copy continuously; publishing is an explicit action (see [page-lifecycle](page-lifecycle.md)).

## Public page

- Reached at `/s/<slug>`. No account required.
- Shows published content only.
- Anyone with the link can view it. It is not listed anywhere and is marked as not to be indexed by search engines.
- If the visitor is signed in as the owner, a thin **Editar** bar links to `/edit`. Visitors do not see it.
