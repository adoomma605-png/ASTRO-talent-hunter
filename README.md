# Talent Hunter — Final

This build uses **Supabase**, not Firebase.

## Included
- `index.html`
- `css/style.css`
- `js/script.js`
- `assets/logo.png`

## Supabase
The project URL and publishable browser key are already configured in `js/script.js`.

The app checks the `talents` table at startup. When the check succeeds, the top badge becomes **SUPABASE CONNECTED** and the browser Console prints:

`[Talent Hunter] Supabase Connected`

### Required Supabase setup
1. Create a table named `talents` with these columns:
   - `id` (uuid or bigint primary key)
   - `name` (text)
   - `phone` (text)
   - `type` (text)
   - `description` (text, optional)
   - `file_type` (text)
   - `media_url` (text)
   - `storage_path` (text)
   - `created_at` (timestamp with time zone, default `now()`)
2. Create a Storage bucket named `talent-media` and make it public if you want the generated media URLs to be directly viewable.
3. Configure the needed RLS / Storage policies for browser inserts, reads, and uploads.

## Testing
Open the deployed site, press `Ctrl + Shift + I`, choose **Console**, then reload the page.
You should see:

`[Talent Hunter] Supabase Connected`

and the top status badge should say **SUPABASE CONNECTED**.
