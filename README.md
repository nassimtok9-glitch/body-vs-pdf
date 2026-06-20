# Body vs PDF — GitHub Pages

موقع ثابت لمقارنات **payload (التطبيق)** مقابل **PDF (الباك إند)** لتقارير Oregistrerat fordon.

**مصدر المحتوى:** [ih-insuranceapp](https://github.com/YOUR_USERNAME/ih-insuranceapp) → `docs/test-references/body-vs-pdf/`

## المحتوى الحالي

| نوع التقرير | السينariوهات |
|-------------|--------------|
| `machineKollision` (kolliosn) | S1–S10 |

**الفهرس:** [index.html](index.html) · [machineKollision/index.html](machineKollision/index.html)

## النشر

1. **Pages:** Settings → Pages → Source: **GitHub Actions**
2. Push إلى `main` يُشغِّل `deploy-pages.yml`
3. URL: عدّل `githubPagesUrl` في [`site-urls.json`](site-urls.json)

## تحديث المحتوى من مشروع التطبيق

```powershell
# من مجلد ih-insuranceapp
.\scripts\sync-body-vs-pdf-site.ps1
cd body-vs-pdf-site
git add .
git commit -m "Sync body-vs-pdf documentation"
git push
```

## Repo منفصل — إعداد أول مرة

```powershell
cd body-vs-pdf-site
git init
git add .
git commit -m "Initial Body vs PDF GitHub Pages site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/body-vs-pdf.git
git push -u origin main
```

## ملاحظات

- لا tokens ولا API keys في HTML
- روابط Field Reference و Test Cases تشير إلى repo التطبيق (راجع `site-urls.json`)
- `.nojekyll` يمنع Jekyll من تجاهل مجلدات تبدأ بـ `_`
