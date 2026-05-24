# Wedding Invitation – Fast Edition

A lightweight, personalised online wedding invitation.  
**No backend, no build tools, no dependencies** – just two HTML files.

---

## Files

| File | Purpose |
|---|---|
| `index.html` | The invitation page guests see |
| `home.html` | Admin link-generator (you use this) |
| `assets/` | Images & video |

---

## How to use

### 1. Deploy
Upload both files + `assets/` folder to:
- GitHub Pages
- Netlify / Vercel (drag-and-drop)
- Any static web host

### 2. Generate links (home.html)
Open `home.html` in your browser.  
Enter the guest's name, choose the invitation type, click **Generate Link**.  
Share the link directly on WhatsApp with one click.

### 3. URL format
```
https://your-site.com/index.html?to=Ramesh+Sharma&type=family
```

| Param | Values | Result on card |
|---|---|---|
| `to` | Any name | Shown on card + greeting |
| `type` | `family` | "With Family" |
| `type` | `single` | "(Only)" |
| `type` | *(omitted)* | No suffix |

---

## Performance improvements over original

- Single self-contained HTML file (no external CSS/JS)
- `fetchpriority="high"` on the above-fold card image
- `loading="lazy"` on all below-fold images
- Sparkles done in CSS, zero JS timers
- No heavy animation loops on body background
- Fonts fetched with `display=swap` so text renders instantly
- All DOM work done in one synchronous pass (no setTimeout hacks)
