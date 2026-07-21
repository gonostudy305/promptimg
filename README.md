# PromptIMG — Landing (GitHub Pages)

Trang bán PromptIMG (static): pitch + bảng giá + **VietQR Techcombank**.

## URL

Sau khi bật Pages: `https://<user>.github.io/promptimg/`

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
