# Hukuk Sınavı Hazırlık Platformu

Bu proje, hukuk sınavlarına hazırlanan adaylar için kapsamlı bir çalışma platformu sunmaktadır. Kullanıcılar farklı hukuk kategorilerinde binlerce soruya erişebilir, kişiselleştirilmiş testler oluşturabilir ve performans analizlerine göre gelişimlerini takip edebilirler.

## Özellikler

- **Kategori Bazlı Çalışma**: Farklı hukuk alanlarında organize edilmiş soru bankaları
- **Kişiselleştirilmiş Testler**: Zorluk seviyesi ve konu alanına göre özelleştirilebilir sınavlar
- **Performans Analizi**: Detaylı istatistikler ve gelişim takibi
- **Kullanıcı Dostu Arayüz**: Modern ve duyarlı tasarım

## Teknoloji Yığını

- **Frontend**: Next.js 15, React 19, TypeScript
- **Stil**: Tailwind CSS
- **Test**: Jest, React Testing Library
- **Veri Yönetimi**: Şu anda mock veri, daha sonra API entegrasyonu
- **Kimlik Doğrulama**: NextAuth.js (gelecek sürümlerde)

## Proje Yapısı

```
src/
├── app/                     # Next.js App Router yapısı
│   ├── page.tsx             # Ana sayfa
│   ├── categories/          # Kategoriler sayfası
│   │   ├── page.tsx
│   │   └── [categoryId]/    # Kategori detay sayfası
│   │       └── page.tsx
│   └── quiz/                # Quiz sayfaları
│       ├── page.tsx
│       └── [id]/
│           └── page.tsx
├── components/              # React bileşenleri
│   ├── ui/                  # Temel UI bileşenleri
│   │   ├── LoadingState.tsx
│   │   └── ErrorState.tsx
│   └── sections/            # Sayfa bölümleri
│       ├── HeroSection.tsx
│       ├── AdvantagesSection.tsx
│       ├── CategoriesSection.tsx
│       └── ...
├── lib/                     # Yardımcı fonksiyonlar ve sabitler
│   ├── constants.ts         # Uygulama sabitleri
│   ├── types.ts             # TypeScript tip tanımlamaları
│   └── mockData/            # Mock veri kaynakları
│       ├── categories.ts
│       ├── topics.ts
│       ├── quizzes.ts
│       └── ...
└── __tests__/               # Test dosyaları
```

## Geliştirme

Bu proje Next.js 15 ile oluşturulmuştur. Geliştirme sunucusunu başlatmak için:

```bash
npm install
npm run dev
```

Uygulama http://localhost:3000 adresinde çalışacaktır.

## Test

Projeyi test etmek için:

```bash
npm test           # Tüm testleri çalıştır
npm run test:watch # Geliştirme sırasında testleri izle
npm run test:coverage # Test kapsama raporunu görüntüle
```

## Deployment

Bu proje Vercel platformunda canlıya alınmak üzere yapılandırılmıştır.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https://github.com/pozitifbascaz/adnanbeyy)  <!-- Reponuzun URL'sini buraya ekleyin -->

Ana dal (örn. `main` veya `master`) güncellendiğinde Vercel otomatik olarak yeni bir sürüm yayınlayacaktır.

## Fazlı Yapı

Proje, aşağıdaki fazlar halinde geliştirilmektedir:

1. **Faz 1**: Temel yapı ve bileşen sisteminin kurulması (Tamamlandı)
2. **Faz 2**: Kategori sayfaları ve mock veri entegrasyonu (Şu Anda Burada)
3. **Faz 3**: Kimlik doğrulama ve API entegrasyonu (Gelecek)
4. **Faz 4**: Quiz işlevselliği, performans optimizasyonu ve son cilalama (Gelecek)

## Erişilebilirlik

Bu uygulama, WCAG 2.1 AA standartlarına uygun olarak geliştirilmektedir. Tüm bileşenler klavye navigasyonu için uygun şekilde yapılandırılmış ve ARIA nitelikleri eklenmiştir.

## Katkıda Bulunma

1. Bu depoyu fork edin
2. Yeni bir özellik dalı oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some amazing feature'`)
4. Dalı push edin (`git push origin feature/amazing-feature`)
5. Bir Pull Request açın

## Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.
