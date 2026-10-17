---
name: template-design
description: Make a poster, social media post, flyer, menu, invitation, quote card, infographic or thumbnail by starting from one of Igly's editable design templates and rewriting its text. Use when the user wants a designed graphic rather than a diagram.
---

# Template design

Igly has thousands of designed, editable templates. Start from one instead of drawing a layout from scratch.

## 1. Find templates
- `list_templates` with a `query` from the request ("bakery menu", "summer sale", "wedding invitation", "quote") and/or a `category` (Posters, Social posts, Business, Food, Travel, Infographics, Video thumbnails...). Use `limit` 8 to 12.
- Match the size to the use: 1080 x 1080 or 1080 x 1350 for feed posts, 1080 x 1920 for stories, 1587 x 2245 for print posters.
- Offer 2 or 3 options in one short line each, or pick the best fit if the user asked you to choose.

## 2. Create from the template
`create_canvas` with `template_id` and a `title`. Keep `canvas_id`.

## 3. Rewrite the copy
- `get_canvas_summary` to see the template's text elements and their ids.
- `update_elements` with new `text` for each, in one call. Keep each text about as long as the original so the layout holds; shorten headlines rather than shrinking fonts.
- Recolor to the user's brand with `fill` on shapes and `color` on text, using the same ids.
- Remove parts that don't apply with `remove_elements`; add missing details (date, address, price) as `type: "text"` matching the nearby font and color.

## 4. Check and deliver
- `get_canvas_summary` again; nudge anything that collides with `update_elements` (`dx`, `dy`) or `arrange`.
- `export_png` (`scale: 2`) for a ready image.
- Photos in templates are part of the design; to swap in the user's own photos they can open the board in the full editor through `open_url`.
