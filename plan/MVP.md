# 📱 Transfer Haber Sistemi - MVP

## 🎯 Proje Özeti
Transfer haberlerini otomatik olarak takip eden, içerik üreten ve yöneten akıllı bir sistem. İki dilde (TR/EN) çalışır ve kullanıcıya hazır Instagram gönderileri sunar.

## 💡 Temel Özellikler

### 1. Otomatik Haber Toplama
- Türkçe ve İngilizce kaynaklardan sürekli tarama
- Transfer detaylarını otomatik çıkarma (ücret, tür)
- 30 dakikada bir güncelleme

### 2. İçerik Üretimi
- AI destekli gönderi metni (TR & EN)
- Oyuncuya özel 3 görsel
- Transfer detaylarını vurgulayan akıllı format

### 3. Web Dashboard
- Responsive tasarım (Mobil/Tablet uyumlu)
- Kolay içerik yönetimi
- Prompt düzenleme özelliği
- Tek tıkla metin kopyalama
- Görsel önizleme ve indirme

### 4. Bildirim Sistemi
- E-posta bildirimleri
- Yeni içerik oluşunca anında bilgi

## 🛠️ Teknoloji Yığını

| Katman     | Teknoloji           | Açıklama                  |
|:-----------|:-------------------|:--------------------------|
| Backend    | Python (Flask)     | Ana uygulama sunucusu     |
| Frontend   | HTML/CSS (Jinja2)  | Kullanıcı arayüzü         |
| AI         | OpenAI GPT-4/3.5   | İçerik üretimi            |
| Görsel     | Bing Image Search  | Oyuncu görselleri         |
| E-posta    | SendGrid           | Bildirim sistemi          |
| Veritabanı | Supabase (PostgreSQL) | Veri depolama         |
| Hosting    | Render.com/Railway | Uygulama barındırma       |

## 📊 Veritabanı Şeması

### posts tablosu

| Alan          | Tür       | Açıklama                        |
|:--------------|:----------|:--------------------------------|
| id            | UUID      | Benzersiz kimlik                |
| title         | TEXT      | Haber başlığı                   |
| content       | TEXT      | Ham haber içeriği               |
| source_lang   | TEXT      | Kaynak dili (tr/en)            |
| source_url    | TEXT      | Haber kaynağı                   |
| player_name   | TEXT      | Oyuncu adı                      |
| transfer_type | TEXT      | Transfer türü                   |
| transfer_fee  | TEXT      | Transfer ücreti                 |
| ai_prompt_tr  | TEXT      | TR içerik promptu               |
| ai_prompt_en  | TEXT      | EN içerik promptu               |
| ai_caption_tr | TEXT      | TR gönderi metni                |
| ai_caption_en | TEXT      | EN gönderi metni                |
| image_urls    | JSONB     | Görsel bağlantıları             |
| created_at    | TIMESTAMP | Oluşturma zamanı                |
| email_sent    | BOOLEAN   | Bildirim durumu                 |

## 💰 Maliyet ve Kaynaklar

### Aylık Tahmini Maliyet
- Hosting: $7 (Render.com Free + Worker)
- AI API: $5 (OpenAI)
- Görsel API: $3 (Bing Search)
- **Toplam**: ~$15/ay

### Ücretsiz Kaynaklar
- SendGrid: 100 email/gün
- Supabase: 500MB veritabanı
- Render.com: Temel hosting

## 🚀 Kurulum Süreci

1. Temel Altyapı
   - Flask uygulaması kurulumu
   - Supabase bağlantısı
   - Şablonların hazırlanması

2. API Entegrasyonları
   - OpenAI API bağlantısı
   - Bing Image Search entegrasyonu
   - SendGrid mail sistemi

3. Güvenlik
   - Basit şifre koruması
   - API anahtarları yönetimi
   - Hata yakalama sistemleri

## 📈 Başarı Kriterleri

- Günlük en az 10 transfer haberi işleme
- %95 doğruluk oranı
- 1 saniyeden kısa sayfa yüklenme süresi
- Mobil cihazlarda sorunsuz çalışma
- Kullanıcı müdahalesi gerektirmeyen işleyiş 

