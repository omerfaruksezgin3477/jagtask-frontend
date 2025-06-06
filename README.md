# JAGTASK Görev Takip Sitesi

JAGTASK, adını jaguardan (JAG) ve görevlerden (TASK) alan, kullanıcıların görevlerini verimli bir şekilde yönetmelerini sağlayan modern bir web uygulamasıdır. Projenin ana teması, bir jaguarın iki zıt yönü üzerine kurulmuştur: aydınlık tarafı temsil eden beyaz jaguar ve karanlık, hedef odaklı tarafı temsil eden siyah jaguar.

Bu platform, kullanıcıların günlük işlerini, uzun vadeli hedeflerini ve ekip çalışmalarını üç farklı ve özelleştirilmiş arayüzde yönetmelerine olanak tanır.

## 📖 Proje Sayfaları ve İşlevleri

Proje toplamda 5 ana sayfadan oluşmaktadır: Giriş, Ana Sayfa ve bu ana sayfadan yönlendirilen üç farklı görev yönetimi kartı (Aydınlık, Karanlık, Ekip).

### 1. 🔐 Login (Giriş ve Kayıt)

Bu sayfa, kullanıcıların sisteme dahil olmasını sağlar.
* **Kullanıcı Kaydı:** Yeni kullanıcılar ad, soyad, e-posta, kullanıcı adı ve şifre ile sisteme kayıt olabilirler.
* **Kullanıcı Girişi:** Kayıtlı kullanıcılar, kullanıcı adı ve şifreleri ile giriş yapabilirler.
* **Dinamik Form Geçişi:** Tek bir bağlantı ile "Giriş Yap" ve "Kayıt Ol" formları arasında kolayca geçiş yapılabilir.
* **Backend Entegrasyonu:** Kayıt ve giriş işlemleri, bir PHP arka planına yapılan `fetch` istekleri ile yönetilir.
* **Yönlendirme:** Başarılı girişin ardından kullanıcılar otomatik olarak ana sayfaya (`JAGTASK.html`) yönlendirilir.
* **Veri Saklama:** Başarılı girişte kullanıcı bilgileri (`user_id`, `username`, `name`, `email`) tarayıcının `localStorage` biriminde saklanır.

### 2. 🏠 Ana Sayfa (JAGTASK)

Burası projenin ana karşılama ekranı ve diğer modüllere geçiş kapısıdır.
* **Sabit Üst Menü:** Sayfanın üst kısmında "JAGTASK" logosu ve adının bulunduğu, sayfa kaydırılsa bile sabit kalan bir menü bulunur.
* **Sosyal Medya Bağlantıları:** Menünün sağ tarafında Instagram, X (Twitter) ve Facebook gibi sosyal medya platformlarına yönlendiren ikonlar yer alır.
* **Yönlendirme Kartları:** Sayfanın merkezinde kullanıcıları farklı modüllere yönlendiren üç adet kart bulunur:
    * **Aydınlık Kart:** "Günlük işler için" sloganıyla, aydınlık tema sayfasına yönlendirir.
    * **Karanlık Kart:** "Hedefleri olanlar için" sloganıyla, karanlık tema sayfasına yönlendirir.
    * **Grup Kartı:** "Grup işleri için" sloganıyla, ekip çalışması sayfasına yönlendirir.
* **Etkileşimli Tasarım:** Kartların üzerine gelindiğinde hafifçe büyüyerek (`transform: scale(1.05)`) kullanıcıya geri bildirimde bulunur.

### 3. 💡 Aydınlık Kart (Günlük Görevler)

Beyaz jaguarı temsil eden bu sayfa, daha çok günlük planlama ve anlık görevler için tasarlanmıştır. "Glassmorphic" (camsı) bir tasarıma sahiptir.
* **Dinamik Takvim:**
    * Bulunulan ayı ve yılı gösterir ve aylar arasında geçiş yapmaya olanak tanır.
    * JavaScript ile oluşturulan takvim, içinde bulunulan günü özel bir renkle vurgular.
    * İçerisinde görev bulunan günler farklı bir renkte işaretlenir.
* **Görev Yönetimi:**
    * Kullanıcılar "Günlük Plan" veya başlık ve açıklamadan oluşan genel görevler ekleyebilirler.
    * Görevler, sol taraftaki açılır/kapanır menüde listelenir.
    * Her görev kolayca silinebilir.
* **Tema Özelleştirme:** Kullanıcılar, "Tema" butonu aracılığıyla sunulan çeşitli arka plan görsellerinden birini seçerek sayfanın görünümünü kişiselleştirebilir. Seçilen tema `localStorage` kullanılarak kaydedilir.
* **Öneri Kutusu:** Kullanıcılar, "Öneri" butonu ile açılan bir pencere aracılığıyla uygulama hakkındaki geri bildirimlerini gönderebilirler.

### 4. 🌙 Karanlık Kart (Hedefler ve Gelişim)

Siyah jaguarı temsil eden bu bölüm, uzun vadeli hedefleri ve kişisel gelişimi izlemek isteyen, motivasyon arayan kullanıcılar için tasarlanmıştır.
* **Alt Menü Sistemi:**
    * Ekranın altındaki logo ikonuna tıklandığında açılan bir menü bulunur.
    * Bu menüdeki linklerin üzerine gelindiğinde, siyah jaguarın gözlerine bir gönderme olarak, renkleri yeşile döner.
    * Menüden "Hedef Ekle", "Gelişimini Ekle" ve "Önemli Ekle" gibi farklı türde kayıtlar oluşturulabilir.
* **Sağ Menü (Listeler):**
    * Ekranın sağ tarafında açılıp kapanabilen bir menüde eklenen tüm kayıtlar listelenir.
    * Kayıtlar; "Görevler", "Önemliler" ve "Gelişmeler" olarak üç ayrı kategoride tutulur.
* **Önemli Görevler:** Görev ekleme ekranındaki yıldız ikonu ile bir görev "Önemli" olarak işaretlenebilir ve ilgili listede görüntülenir.
* **Kişiselleştirme:** Aydınlık kartta olduğu gibi, burada da kullanıcılar için özenle seçilmiş karanlık temalar  ve bir öneri kutusu mevcuttur.

### 5. 👥 Ekip Kartı (Ortak Çalışma)

Bu sayfa, birden fazla kişinin dahil olduğu projeleri ve görevleri yönetmek için tasarlanmıştır.
* **Katılımcı Yönetimi:**
    * Kullanıcılar, "Katılımcılar" menüsünden ekibe yeni üyeler ekleyebilir.
    * Eklenen her katılımcı sağ menüde listelenir ve istenildiğinde silinebilir.
* **Görev Atama:**
    * Yeni bir görev oluşturulurken, bu görevin hangi katılımcılara atanacağı seçilebilir.
    * Bir göreve tıklandığında açılan detay penceresinde, göreve atanan kişiler görüntülenebilir ve atamalar güncellenebilir.
* **Görev Detayları ve Güncelleme:**
    * Listelenen bir göreve tıklandığında, başlığını, açıklamasını, önem durumunu ve atanmış katılımcıları gösteren bir detay penceresi açılır.
    * Kullanıcılar bu pencere üzerinden görevin önem durumunu  veya atanan kişileri güncelleyebilirler.
* **Yapı:** Sayfa; sol menüde görev listeleri [cite: 279], ortada takvim  ve sağ menüde katılımcı listesi  olmak üzere üç sütunlu bir düzene sahiptir.

## 🛠️ Teknik Yapı

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **Backend:** PHP (Sadece kullanıcı kayıt ve giriş işlemleri için)

Link: [JAGTASK]([https://vercel.com](https://jagtask-frontend.vercel.app/html_pages/loding.k%C4%B1sm%C4%B1.html))
