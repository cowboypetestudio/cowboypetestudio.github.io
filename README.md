# Pedro's Wish List

A small static website for my birthday wish list. Hosted on GitHub Pages.

## Files in this repo

- `index.html` — the public website (what visitors see)
- `products.json` — the list of products. **This is the only file you edit to add/remove items.**

## How to add a new product

1. Open `products.json` on github.com.
2. Click the **pencil icon** (top right) to edit.
3. Add a new block inside the square brackets `[ ... ]`. Copy an existing one and change the values.

   Each product looks like this:

   ```json
   {
     "name": "Library Reading Lamp",
     "brand": "Anglepoise",
     "price": "$329",
     "spec": "Type 75 / Margaret Howell",
     "url": "https://example.com/lamp",
     "image": ""
   }
   ```

4. Make sure each product block ends with `},` — except the last one in the list, which has just `}`.
5. Scroll down, click **Commit changes**.
6. Wait ~1 minute. Refresh your live site. The new product is there.

## How to remove a product

Open `products.json`, delete the whole block (from `{` to `}` and the comma after it), commit changes.

## How to reorder products

Cut and paste blocks up or down in the file. The order in `products.json` is the order on the page.

## Field guide

| Field   | Required? | Notes                                                               |
| ------- | --------- | ------------------------------------------------------------------- |
| `name`  | yes       | The product name shown in the grid.                                 |
| `brand` | no        | Brand or maker. Shown under the image.                              |
| `price` | no        | Free-form text, e.g. `"$200"` or `"€150"`. Shown next to the name.  |
| `spec`  | no        | Short detail like size or color.                                    |
| `url`   | no        | If filled in, the product becomes a clickable link.                 |
| `image` | no        | A direct URL to a product image (`.jpg` / `.png`).                  |

If a field is empty, just leave the quotes empty: `"image": ""`.

## Common mistakes

- **Missing comma** between two products → page won't load. Each product block ends in `},` except the last.
- **Extra comma after the last product** → also breaks. The last product ends in just `}`.
- **Curly quotes vs straight quotes** → JSON requires straight quotes `"like this"`. If you copy text from a Word doc you may get curly ones; replace them.

If the page goes blank, undo your last commit on github.com (Commits → click the bad one → Revert).
