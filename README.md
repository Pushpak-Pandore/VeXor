# REVS3C - Cybersecurity Hugo Site

## 🚀 Quick Start

Hugo site (hextra theme) for Windows/AD/SIEM/C2 notes.

Server running: http://localhost:1313 (live reload active)

### Verified Successful Steps (Windows 10)
1. **Hugo**: v0.159.2 at `P:\hugo\hugo.exe` ✓ (`P:\hugo\hugo.exe version`)
2. **Go**: v1.26.1 ✓ (`go version`)
3. **Modules**: Tidied ✓ (`P:\hugo\hugo.exe mod tidy`)
4. **Dev Server**: Running at http://localhost:1313 ✓ (`P:\hugo\hugo.exe server -D -F --bind=127.0.0.1 --disableKinds=rss,robotsTXT,sitemap`)
   - 29 pages built, live reload ✓

### Prerequisites (if starting fresh)
- Hugo extended (download https://github.com/gohugoio/hugo/releases)
- Go 1.21+

### To Restart Server
```cmd
# Stop current (Ctrl+C), then:
P:\hugo\hugo.exe server -D -F --bind=127.0.0.1 --disableKinds=rss,robotsTXT,sitemap
```

### Build Static Site
```cmd
P:\hugo\hugo.exe --minify
```
Serve `public/`:
```cmd
cd public
python -m http.server 8000
```
View: http://localhost:8000
```cmd
P:\hugo\hugo.exe --minify
```
Serve `public/` (e.g. `python -m http.server 8000`).

### Optional: Fix RSS Error
In `hugo.yaml`, add under `params:`:
```
authors:
  default:
    name: Pushpak Pandore
    email: pushpak.pandore@gmail.com
```
Remove top-level `Author:`.

### Add to PATH (permanent)
Add `P:\hugo` to Windows PATH, then use `hugo` directly.

Enjoy the site!
