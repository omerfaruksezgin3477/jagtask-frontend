# JAGTASK Görev Takip Sitesi

JAGTASK, adını jaguardan (JAG) ve görevlerden (TASK) alan, kullanıcıların görevlerini verimli bir şekilde yönetmelerini sağlayan modern bir web uygulamasıdır. Projenin ana teması, bir jaguarın iki zıt yönü üzerine kurulmuştur: aydınlık tarafı temsil eden beyaz jaguar ve karanlık, hedef odaklı tarafı temsil eden siyah jaguar.

Bu platform, kullanıcıların günlük işlerini, uzun vadeli hedeflerini ve ekip çalışmalarını üç farklı ve özelleştirilmiş arayüzde yönetmelerine olanak tanır.

## 📖 Proje Sayfaları ve İşlevleri

Proje toplamda 5 ana sayfadan oluşmaktadır: Giriş, Ana Sayfa ve bu ana sayfadan yönlendirilen üç farklı görev yönetimi kartı (Aydınlık, Karanlık, Ekip).

### 1. 🔐 Login (Giriş ve Kayıt)

[cite_start]Bu sayfa, kullanıcıların sisteme dahil olmasını sağlar.
* [cite_start]**Kullanıcı Kaydı:** Yeni kullanıcılar ad, soyad, e-posta, kullanıcı adı ve şifre ile sisteme kayıt olabilirler.
* [cite_start]**Kullanıcı Girişi:** Kayıtlı kullanıcılar, kullanıcı adı ve şifreleri ile giriş yapabilirler.
* [cite_start]**Dinamik Form Geçişi:** Tek bir bağlantı ile "Giriş Yap" ve "Kayıt Ol" formları arasında kolayca geçiş yapılabilir.
* [cite_start]**Backend Entegrasyonu:** Kayıt ve giriş işlemleri, bir PHP arka planına yapılan `fetch` istekleri ile yönetilir.
* [cite_start]**Yönlendirme:** Başarılı girişin ardından kullanıcılar otomatik olarak ana sayfaya (`JAGTASK.html`) yönlendirilir.
* [cite_start]**Veri Saklama:** Başarılı girişte kullanıcı bilgileri (`user_id`, `username`, `name`, `email`) tarayıcının `localStorage` biriminde saklanır.

### 2. 🏠 Ana Sayfa (JAGTASK)

Burası projenin ana karşılama ekranı ve diğer modüllere geçiş kapısıdır.
* [cite_start]**Sabit Üst Menü:** Sayfanın üst kısmında "JAGTASK" logosu ve adının bulunduğu, sayfa kaydırılsa bile sabit kalan bir menü bulunur.
* [cite_start]**Sosyal Medya Bağlantıları:** Menünün sağ tarafında Instagram, X (Twitter) ve Facebook gibi sosyal medya platformlarına yönlendiren ikonlar yer alır.
* **Yönlendirme Kartları:** Sayfanın merkezinde kullanıcıları farklı modüllere yönlendiren üç adet kart bulunur:
    * [cite_start]**Aydınlık Kart:** "Günlük işler için" sloganıyla, aydınlık tema sayfasına yönlendirir.
    * [cite_start]**Karanlık Kart:** "Hedefleri olanlar için" sloganıyla, karanlık tema sayfasına yönlendirir.
    * [cite_start]**Grup Kartı:** "Grup işleri için" sloganıyla, ekip çalışması sayfasına yönlendirir.
* [cite_start]**Etkileşimli Tasarım:** Kartların üzerine gelindiğinde hafifçe büyüyerek (`transform: scale(1.05)`) kullanıcıya geri bildirimde bulunur.

### 3. 💡 Aydınlık Kart (Günlük Görevler)

Beyaz jaguarı temsil eden bu sayfa, daha çok günlük planlama ve anlık görevler için tasarlanmıştır. [cite_start]"Glassmorphic" (camsı) bir tasarıma sahiptir.
* **Dinamik Takvim:**
    * [cite_start]Bulunulan ayı ve yılı gösterir ve aylar arasında geçiş yapmaya olanak tanır.
    * [cite_start]JavaScript ile oluşturulan takvim, içinde bulunulan günü özel bir renkle vurgular.
    * [cite_start]İçerisinde görev bulunan günler farklı bir renkte işaretlenir.
* **Görev Yönetimi:**
    * [cite_start]Kullanıcılar "Günlük Plan" veya başlık ve açıklamadan oluşan genel görevler ekleyebilirler.
    * [cite_start]Görevler, sol taraftaki açılır/kapanır menüde listelenir.
    * [cite_start]Her görev kolayca silinebilir.
* [cite_start]**Tema Özelleştirme:** Kullanıcılar, "Tema" butonu aracılığıyla sunulan çeşitli arka plan görsellerinden birini seçerek sayfanın görünümünü kişiselleştirebilir. [cite_start]Seçilen tema `localStorage` kullanılarak kaydedilir.
* [cite_start]**Öneri Kutusu:** Kullanıcılar, "Öneri" butonu ile açılan bir pencere aracılığıyla uygulama hakkındaki geri bildirimlerini gönderebilirler.

### 4. 🌙 Karanlık Kart (Hedefler ve Gelişim)

Siyah jaguarı temsil eden bu bölüm, uzun vadeli hedefleri ve kişisel gelişimi izlemek isteyen, motivasyon arayan kullanıcılar için tasarlanmıştır.
* **Alt Menü Sistemi:**
    * [cite_start]Ekranın altındaki logo ikonuna tıklandığında açılan bir menü bulunur.
    * [cite_start]Bu menüdeki linklerin üzerine gelindiğinde, siyah jaguarın gözlerine bir gönderme olarak, renkleri yeşile döner.
    * [cite_start]Menüden "Hedef Ekle", "Gelişimini Ekle" ve "Önemli Ekle" gibi farklı türde kayıtlar oluşturulabilir.
* **Sağ Menü (Listeler):**
    * [cite_start]Ekranın sağ tarafında açılıp kapanabilen bir menüde eklenen tüm kayıtlar listelenir.
    * Kayıtlar; [cite_start]"Görevler", "Önemliler" ve "Gelişmeler" olarak üç ayrı kategoride tutulur.
* [cite_start]**Önemli Görevler:** Görev ekleme ekranındaki yıldız ikonu ile bir görev "Önemli" olarak işaretlenebilir ve ilgili listede görüntülenir.
* [cite_start]**Kişiselleştirme:** Aydınlık kartta olduğu gibi, burada da kullanıcılar için özenle seçilmiş karanlık temalar  [cite_start]ve bir öneri kutusu mevcuttur.

### 5. 👥 Ekip Kartı (Ortak Çalışma)

Bu sayfa, birden fazla kişinin dahil olduğu projeleri ve görevleri yönetmek için tasarlanmıştır.
* **Katılımcı Yönetimi:**
    * [cite_start]Kullanıcılar, "Katılımcılar" menüsünden ekibe yeni üyeler ekleyebilir.
    * [cite_start]Eklenen her katılımcı sağ menüde listelenir ve istenildiğinde silinebilir.
* **Görev Atama:**
    * [cite_start]Yeni bir görev oluşturulurken, bu görevin hangi katılımcılara atanacağı seçilebilir.
    * [cite_start]Bir göreve tıklandığında açılan detay penceresinde, göreve atanan kişiler görüntülenebilir ve atamalar güncellenebilir.
* **Görev Detayları ve Güncelleme:**
    * [cite_start]Listelenen bir göreve tıklandığında, başlığını, açıklamasını, önem durumunu ve atanmış katılımcıları gösteren bir detay penceresi açılır.
    * [cite_start]Kullanıcılar bu pencere üzerinden görevin önem durumunu  [cite_start]veya atanan kişileri güncelleyebilirler.
* [cite_start]**Yapı:** Sayfa; sol menüde görev listeleri [cite: 279][cite_start], ortada takvim  [cite_start]ve sağ menüde katılımcı listesi  olmak üzere üç sütunlu bir düzene sahiptir.

## 🛠️ Teknik Yapı

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **Backend:** PHP (Sadece kullanıcı kayıt ve giriş işlemleri için)
* [cite_start]**Veri Depolama:** Tarayıcı tabanlı verilerin (görevler, katılımcılar, tema tercihleri vb.) saklanması için `localStorage` aktif olarak kullanılmaktadır.