# Günce — Kişisel Takip

Görev, günlük plan, beslenme/makro, su, spor ve kilo takibi yapan tek dosyalık web uygulaması.

## Kullanım
- `Takip.dc.html` dosyasını çift tıklayıp tarayıcıda aç. (`support.js` aynı klasörde olmalı.)
- İlk açılışta React kütüphanesi CDN'den yüklenir, bu yüzden **ilk açılışta internet gerekir**. Sonrasında veriler tarayıcının `localStorage`'ında saklanır.
- Verilerin bu tarayıcıya/cihaza özeldir. Yedek almak için: **Profil & hedefler → Yedek indir**. Başka cihaza taşımak için aynı yerden **Yedek yükle**.

## Bulut senkron (her cihazda kaldığı yerden devam)
Veriler varsayılan olarak tarayıcıya kaydedilir. Cihazlar arası otomatik senkron için **JSONBin** kullanılır:

1. [jsonbin.io](https://jsonbin.io) → ücretsiz hesap aç.
2. **API Keys** bölümünden **Master Key**'i kopyala.
3. **Bins → Create Bin** ile `{}` içerikli bir bin oluştur, **Bin ID**'yi kopyala.
4. Uygulamada **Profil & hedefler → Bulut senkron** alanına Bin ID + Master Key gir, **Bağlan & senkronize et**'e bas.
5. Aynı Bin ID + Key'i kullandığın her cihaza (telefon, başka bilgisayar) gir — veriler otomatik senkron olur.

Senkron mantığı "en son kaydedilen kazanır" (last-write-wins). Anahtar koda gömülü değildir; her cihazın kendi tarayıcısında saklanır.

## Yayınlama (GitHub Pages)
Repo: https://github.com/YusufUzun03/PersonalTracker — **Settings → Pages → Branch: main / root** seçince
`https://yusufuzun03.github.io/PersonalTracker/Takip.dc.html` adresinden her cihazdan açılır.

## Notlar
- Kullanmadığın modülleri **Modüller** ekranından kapatabilirsin (veriler silinmez, sadece gizlenir).
- Profil ve günlük hedefler (kalori/protein/su/antrenman) başlangıçta ayarlanmıştır; **Profil & hedefler** ekranından güncelleyebilirsin.
