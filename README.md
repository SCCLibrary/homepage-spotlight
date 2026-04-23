# homepage-spotlight# SCC Library Spotlight — Staff Guide

Welcome! This guide explains how to update the three featured cards on the library homepage. **No coding required.** Everything happens in GitHub through your web browser.

---

## One-time setup (first visit only)

1. Create a free GitHub account at [github.com/signup](https://github.com/signup) using your library email
2. Send your GitHub username to Lauren at Lbryant@shoreline.edu so you can be added as a collaborator
3. Accept the email invitation you'll receive from GitHub

That's it for setup — you only do this once.

---

## How the spotlight works

The widget shows the **first three cards** listed in a single file called `cards.json`. To update what appears on the homepage, you'll do two things:

1. Upload your image to the `images/` folder
2. Edit `cards.json` to point to that image and add a title, description, and link

Updates appear on the library website within about one minute.

---

## Updating a card — step by step

### Step 1: Upload your image

1. Go to the repository on GitHub
2. Click the **`images`** folder
3. Click **Add file** → **Upload files**
4. Drag your image into the box, or click to browse
5. Scroll down and click the green **Commit changes** button

**Image tips:**
- Recommended size: around 1456 x 480 pixels (landscape orientation)
- File format: `.jpg`, `.png`, or `.webp`
- Keep file size under 500 KB if possible — large files slow down the page
- Use descriptive filenames: `study-rooms-fall-2026.jpg`, not `IMG_8472.jpg`

### Step 2: Edit the cards.json file

1. Go back to the main page of the repository
2. Click the file named **`cards.json`**
3. Click the **pencil icon** (✏️) in the top-right to edit
4. Update one of the three card entries to match your new image
5. Scroll down and click **Commit changes**

### The four fields you can edit per card

| Field | What it does |
|---|---|
| `image` | The filename of the image in the `images/` folder |
| `alt` | A short description of the image for screen readers (**required for accessibility**) |
| `title` | The bold heading shown on the card |
| `description` | The short paragraph below the title (keep it under ~150 characters) |
| `link` | Where the card takes a user when clicked |

### Example

```json
{
  "image": "new-study-nook.jpg",
  "alt": "A cozy reading nook with comfortable chairs and natural light",
  "title": "New Quiet Study Nook",
  "description": "Our newly renovated quiet study area is now open on the second floor.",
  "link": "https://sccwa.libguides.com/spaces"
}
```

---

## Writing good alt text (important!)

Alt text is read aloud to people who use screen readers. It should **describe what's in the image**, not repeat the title.

- ✅ Good: `"Two students reading books at a sunlit library table"`
- ❌ Not useful: `"Library photo"` or `"Academic Databases"` (that's what the title already says)

If the image is purely decorative and adds no information, you can leave the `alt` field as `""` (empty quotes).

---

## A few ground rules

- **Don't delete the `cards.json` file** — edit it instead. If it goes missing, the widget breaks.
- **Keep exactly three cards** in the file for best visual results. The widget will only show the first three regardless, but keeping it tidy helps everyone.
- **Commit messages are public.** Write something descriptive like "Updated fall databases card" rather than leaving the default.
- **When in doubt, ask before committing.** Edits go live within a minute, so it's worth a second look.

---

## Troubleshooting

**My card isn't showing up.**
Double-check that the `image` field matches the exact filename you uploaded, including capitalization and the file extension. `Photo.JPG` and `photo.jpg` are different to GitHub.

**The widget shows an error message.**
The `cards.json` file probably has a typo — usually a missing comma or quote mark. GitHub will sometimes warn you about this when editing. If you get stuck, revert to the previous version using the "History" button on the file.

**The old card is still showing.**
Give it about 60 seconds and refresh the page. If it still hasn't updated after a few minutes, try a hard refresh (Ctrl+Shift+R on Windows, Cmd+Shift+R on Mac).

---

Questions? Contact [repo owner / library web coordinator].
