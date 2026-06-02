# 📚 Miyagical Library

A personal book library hosted on GitHub Pages. Each book is represented by its cover image and links directly to its hosted reading page.

---

## Live site

Once deployed: `https://miyagical.github.io/YOUR-REPO-NAME/`

---

## Folder structure

```
your-repo/
├── index.html          ← the whole site lives here
├── README.md
└── covers/             ← drop cover images here (first page of each book)
    ├── jekyll-hyde.jpg
    ├── animal-farm.jpg
    └── ...
```

---

## Adding a new book

Open `index.html` and find this comment:

```
▼▼▼  ADD MORE BOOKS BELOW THIS LINE  ▼▼▼
```

Copy the template block that follows it and fill in:

| Field | What to put |
|---|---|
| `href` | `https://miyagical.github.io/YOUR-REPO-NAME/` |
| `data-title` | Full title — used by the search bar |
| `data-author` | Author name — used by the search bar |
| `data-genre` | One word: `fiction`, `history`, `horror`, etc. — a filter button appears automatically |
| `ph-title` / `ph-author` | What shows on the placeholder card before you have a cover |

---

## Adding a cover image

1. Export / screenshot the **first page** of the book as a JPG or PNG
2. Drop it into the `covers/` folder (e.g. `covers/animal-farm.jpg`)
3. In the book's card, **replace** the entire `<div class="cover-placeholder">…</div>` block with:
   ```html
   <img src="covers/animal-farm.jpg" alt="Animal Farm">
   ```
4. **Delete** the `<span class="ribbon">Soon</span>` line right below it
5. Save and push — done!

---

## Adding a new genre

You don't need to do anything special. Just use a new word in `data-genre="…"` and a filter button for it appears in the header automatically.

Current genres: `horror` · `fiction` · `history`

---

## URL pattern for book repos

All book links follow this pattern:

```
https://miyagical.github.io/REPO-NAME/
```

If the book uses paginated reading, add `?page=1`:

```
https://miyagical.github.io/Strange-Case-of-Dr-Jekyll-and-Mr-Hyde/?page=1
```

---

## Deploying to GitHub Pages

1. Create a repo (e.g. `library`)
2. Push all files including `covers/`
3. Go to **Settings → Pages**
4. Set source to **Deploy from branch → main → / (root)**
5. Your site is live at `https://miyagical.github.io/library/`

---

## Current books

| # | Title | Author | Genre | Cover ready? |
|---|---|---|---|---|
| 1 | Strange Case of Dr Jekyll and Mr Hyde | Robert Louis Stevenson | horror | ⬜ |
| 2 | Animal Farm | George Orwell | fiction | ⬜ |
| 3 | Europe's History | Unknown | history | ⬜ |

*(Update this table as you add books — it helps you track what still needs a cover)*
