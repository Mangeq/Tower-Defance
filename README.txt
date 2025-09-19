# Top-Down Wave Survival Game

## Oyun Açıklaması
Bu proje, Unity ile geliştirilmiş bir top-down (üstten görünüşlü) dalga tabanlı hayatta kalma oyunudur. Oyuncu, bir karakteri kontrol ederek gelen düşman dalgalarına karşı mücadele eder. Her dalgada farklı düşman tipleri ve bir boss ile karşılaşılır. Oyuncu, kılıç ve ateş topu saldırılarıyla düşmanları yok edebilir, canı sıfırlandığında oyun sona erer ve tekrar başlatılabilir.

## Oyun Mekanikleri
- **Karakter Kontrolü:** WASD ile hareket, sol mouse tıkı ile kılıç saldırısı, otomatik ateş topu fırlatma.
- **Dalga Sistemi:** Düşmanlar belirli aralıklarla ve dalga başına sınırlı sayıda spawn olur. Boss dalgası da mevcuttur.
- **Düşman Yapay Zekası:** Düşmanlar doğrudan oyuncuya veya base'e doğru hareket eder.
- **Can ve UI:** Oyuncunun canı kalp ikonlarıyla gösterilir, can azalınca ikonlar kaybolur.
- **I-Frame:** Hasar alındıktan sonra kısa süreli dokunulmazlık ve görsel yanıp sönme efekti.
- **Oyun Sonu:** Oyuncu veya base yok olursa oyun durur ve tekrar başlatılabilir.

## Kullanılan Unity Sürümü
- **Unity 2023.3.62f1 LTS**  
  (Proje .NET Framework 4.7.1 ve C# 9.0 ile uyumlu şekilde geliştirilmiştir.)

## Varsayımlar
- Tüm düşman prefablarının ve base objesinin sahnede ve Inspector'da doğru şekilde atanmış olduğu varsayılmıştır.
- Oyuncu objesinde `"Player"` tag'i, base objesinde `"Base"` tag'i kullanılmaktadır.
- UI elemanları (kalpler, login panel, butonlar) sahnede hazır ve doğru isimlendirilmiştir.
- Oyun tek sahnede oynanacak şekilde tasarlanmıştır.
- Tüm scriptler, ilgili GameObject'lere atanmıştır.

## Geliştirme Süreci
- **Proje Planı:** Öncelikle temel karakter ve düşman hareketi, dalga sistemi ve saldırı mekanikleri tasarlandı.
- **Script Yapısı:** Her ana fonksiyon için ayrı scriptler (CharacterController2D, Enemy, EnemySpawner, GameManager, Base, Fireball) oluşturuldu.
- **Oyun Akışı:** GameManager üzerinden oyun başlatma, dalga yönetimi ve oyun sonu kontrolleri sağlandı.
- **Test ve Debug:** Sahnede prefab ve UI referansları kontrol edildi, hata ayıklama için Debug.Log kullanıldı.
- **Görsel ve Ses:** Basit animasyonlar ve ses efektleri eklendi, görsel geri bildirimler (yanıp sönme, kalp ikonları) ile desteklendi.
- **Kapsam:** Proje, ön mülakat için temel oyun mekaniklerini ve kod organizasyonunu gösterecek şekilde tamamlandı.

## Dosya Yapısı
- `Assets/Scripts/CharacterController2D.cs` : Oyuncu hareketi ve saldırı mekanikleri
- `Assets/Scripts/Enemy.cs` : Düşman davranışları ve hasar sistemi
- `Assets/Scripts/EnemySpawner.cs` : Dalga ve düşman spawn yönetimi
- `Assets/Scripts/GameManager.cs` : Oyun akışı ve UI kontrolü
- `Assets/Scripts/Base.cs` : Base objesi ve hasar yönetimi
- `Assets/Scripts/Fireball.cs` : Ateş topu saldırısı

## Nasıl Başlatılır?
1. Projeyi Unity 2021.3 LTS ile açın.
2. Sahnede gerekli prefab ve UI objelerinin atandığından emin olun.
3. Play tuşuna basarak oyunu başlatın.

---

**Hazırlayan:**  
Emir Çalışkan  
emircaliskano1@gmail.com
Tarih: Eylül 19, 2025