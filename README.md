# Kitap Yönetim Sistemi (Book Management API)

Bu proje, kitap yönetimi için temel CRUD (Oluşturma, Okuma, Güncelleme, Silme) işlemleri sağlayan bir RESTful API uygulamasıdır. 
Proje, C# ve .NET Core kullanılarak geliştirilmiştir ve SQLite veritabanını kullanmaktadır.

## Özellikler

- Kitap ekleme, silme, güncelleme ve listeleme işlemleri yapılabilir.
- Kitap bilgileri aşağıdaki özellikleri içerir:
  - **Başlık (Title)**
  - **Yazar (Author)**
  - **Yayın Yılı (Year)**
  - **Tür (Genre)**

## Kullanılan Teknolojiler

- **.NET Core 6+**
- **Entity Framework Core** (Veritabanı işlemleri için)
- **SQLite** (Hafif veritabanı)
- **Swagger** (API dokümantasyonu için)

## API Endpointleri

| Metot  | Endpoint              | Açıklama                |
|--------|-----------------------|-------------------------|
| GET    | /api/books           | Tüm kitapları getir     |
| GET    | /api/books/{id}      | Belirli bir kitabı getir|
| POST   | /api/books           | Yeni bir kitap ekle     |
| PUT    | /api/books/{id}      | Mevcut kitabı güncelle  |
| DELETE | /api/books/{id}      | Bir kitabı sil          |

## Proje Nasıl Çalıştırılır?

1. **Projeyi Klonlayın**
```bash
https://github.com/kullanici_adi/BookManagementApi.git
```

2. **Gerekli Bağımlılıkları Yükleyin**
```bash
dotnet restore
```

3. **Veritabanını Oluşturun**
```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
```

4. **Uygulamayı Çalıştırın**
```bash
dotnet run
```

5. **Swagger ile Test Edin**
Tarayıcınızda şu adrese gidin: `https://localhost:5001/swagger`

## Lisans
Bu proje MIT Lisansı ile lisanslanmıştır.
