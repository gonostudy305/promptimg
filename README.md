# PromptIMG — Landing (GitHub Pages)

Trang bán PromptIMG (static): pitch + bảng giá + **VietQR Techcombank**.

## URL

- Repo: https://github.com/gonostudy305/promptimg  
- GitHub Pages: https://gonostudy305.github.io/promptimg/  
- Custom (user site CNAME): http://gonovn.me/promptimg/  

Nếu mở ra **526 Cloudflare**: vào Cloudflare → SSL/TLS → mode **Full** (không Flexible), và DNS `gonovn.me` trỏ đúng GitHub Pages. Source đã `built` trên GitHub.

## Local preview

Mở `index.html` trong browser, hoặc:

```bash
npx --yes serve .
```

## Cấu hình

Trong `index.html`, block `CONFIG`:

- `CONTACT_EMAIL` — email nhận xác nhận CK (mở mailto). Để trống = copy clipboard.
- `BANK` / `PRODUCTS` — STK và giá VND.

## Deploy

Repo này **chỉ** chứa landing public (không chứa source kit / license engine).
