# PromptIMG — Landing (GitHub Pages)

Trang bán PromptIMG (static): pitch + bảng giá + **VietQR Techcombank**.

## URL

| | |
|--|--|
| **Custom domain** | **https://img.gonovn.me/** |
| Repo | https://github.com/gonostudy305/promptimg |
| Fallback | https://gonostudy305.github.io/promptimg/ |

GitHub Pages đã set `cname: img.gonovn.me` + file `CNAME` trong repo.

---

## DNS trên Cloudflare (bạn cần thêm 1 record)

Domain `gonovn.me` đang trỏ Cloudflare. Hiện **`img.gonovn.me` chưa có DNS** → cần tạo:

### Record

| Type | Name | Target / Content | Proxy status |
|------|------|------------------|--------------|
| **CNAME** | `img` | `gonostudy305.github.io` | **DNS only** (grey cloud) lúc setup |

### Các bước Cloudflare

1. Đăng nhập [dash.cloudflare.com](https://dash.cloudflare.com) → zone **gonovn.me**  
2. **DNS** → **Add record**  
3. Type **CNAME**, Name **`img`**, Target **`gonostudy305.github.io`**  
4. Proxy: **Off (DNS only)** cho đến khi GitHub hiện DNS check xanh  
5. **SSL/TLS** → Overview → mode **Full** (không dùng Flexible — hay gây 526)  
6. Đợi 1–30 phút → mở https://img.gonovn.me/  
7. GitHub → repo **promptimg** → Settings → Pages → **Enforce HTTPS** (khi domain verified)

### Kiểm tra DNS

```bash
nslookup img.gonovn.me
# kỳ vọng CNAME → gonostudy305.github.io
```

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
