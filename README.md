# Melisa Çiçek Soyubey – Portföy

Kişisel portföy sitesi: mouse ile renklenen arka plan, GitHub projeleri, “Bana bir şey sor” FAQ, Hakkımda / Projeler / Skills / İletişim bölümleri.

## Kurulum

1. **Ortam değişkenleri:** `.env.example` dosyasını `.env.local` olarak kopyalayın. `GITHUB_TOKEN` ve `GITHUB_USERNAME` değerlerini doldurun (isteğe bağlı: `GEMINI_API_KEY`, `DATABASE_URL`). Token’ı asla repoda paylaşmayın; `.env.local` zaten `.gitignore` içindedir.
2. **Avatar görselleri:** Ana sayfadaki profil fotoğrafı için `public/avatar1.jpg` kullanılır. İsterseniz `public/avatar2.jpg` ve `public/avatar3.jpg` dosyalarını da ekleyebilirsiniz (ileride carousel vb. için kullanılabilir).

## Getting Started

Önce geliştirme sunucusunu çalıştırın:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Build ve yayınlama

Proje **statik export kullanmaz**. "Bana bir şey sor" bölümü `/api/ask` API route'u ile çalıştığı için sitenin Node.js çalıştırabilen bir ortamda yayınlanması gerekir. Bu nedenle GitHub Pages gibi yalnızca statik dosya sunan servisler uygun değildir.

1. **Build alın:** `npm run build`
   - Önce `prebuild` adımı GitHub'dan repo listesini ve README'leri çeker (`GITHUB_TOKEN` ve `GITHUB_USERNAME` gerekir).
   - Ardından Next.js uygulamayı `.next` klasörüne derler.

2. **Çalıştırın:** `npm start` (production sunucusu, varsayılan port 3000).

3. **Yayınlama:** Vercel (önerilir) veya Next.js destekli bir platform (ör. Netlify'ın Next.js runtime'ı) kullanın. Ortam değişkenlerini (`GITHUB_TOKEN`, `GITHUB_USERNAME`, `GEMINI_API_KEY`, `DATABASE_URL`) platformun ayarlarından girin.

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
