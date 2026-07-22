# PromptIMG — Landing (GitHub Pages)

Trang bán PromptIMG (static): pitch + bảng giá + **VietQR Techcombank**.

## URL

| | |
|--|--|
| **Custom domain** | **https://img.gonovn.me/** ✅ SSL Let’s Encrypt |
| Repo | https://github.com/gonostudy305/promptimg |
| Fallback | https://gonostudy305.github.io/promptimg/ |

GitHub Pages: `cname: img.gonovn.me` · `https_enforced: true` · cert CN=`img.gonovn.me`.

---

## DNS (Cloudflare) — đã cấu hình

| Type | Name | Target | Proxy |
|------|------|--------|-------|
| **CNAME** | `img` | `gonostudy305.github.io` | **DNS only** (grey cloud) |

Giữ proxy **tắt** (hoặc SSL Cloudflare = **Full**) để không đụng cert GitHub.

Nếu SSL lại lỗi: Settings → Pages → Remove custom domain → Add lại `img.gonovn.me` → đợi cert `approved` → Enforce HTTPS.

---

## Local preview

```bash
npx --yes serve .
# hoặc mở index.html
```

## Cấu hình trang

Trong `index.html` (block CONFIG):

- `CONTACT_EMAIL` — nhận xác nhận CK  
- `BANK` / `PRODUCTS` — STK & giá  

## Deploy

```bash
git add -A
git commit -m "update landing"
git push origin main
```

Chỉ landing public — không ship source kit / license engine.
