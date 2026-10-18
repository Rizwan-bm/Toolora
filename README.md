readme = """# Toolora. AI Tools Showcase

## Run the website

1. Unzip `ai_tools_showcase_source.zip`.

2. Open `index.html` in Chrome, Edge or Firefox.

No setup or building is needed. You need an internet connection for Bootstrap and Google Fonts from CDNs.

## Features

- Responsive Bootstrap 5 layout

- AI tool cards with direct provider links

- Search and category filters

- Gradient hero section and hover animations

- Mobile-friendly navigation

"""

(base / "index.html").write_text(html, encoding="utf-8")

(base / "README.md").write_text(readme, encoding="utf-8")

zip_path = Path("/mnt/data/ai_tools_showcase_source.zip")

with zipfile.ZipFile(zip_path, "w" zipfile.ZIP_DEFLATED), as zf:

zf.write(base / "index.html" "index.html")

zf.write(base / "README.md" "README.md")

print("Created index.html and ZIP package.")
