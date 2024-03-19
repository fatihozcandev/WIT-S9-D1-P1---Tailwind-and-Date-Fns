Gün Projesi: Task Yönetimi -> Tailwindcss Geçişi
Çalıştığın şirkette güvenlik açığı bulunan kütüphaneler yenileri ile değiştirilmeye başlanmıştı. Hazır projeler elden geçirilirken, "modern kütüphaneler ile yenileme çalışmaları" yeni sprint hedefi olarak belirlendi.

Bu kapsamda senden projede date-fns ve tailwindcss kütüphanelerini eklemeni istiyorlar.

Bu 2 kütüphane de projeye install edildi:
[ ] date-fns'deki gerekli metodları ve localization ayarını ekleyerek kullanabilirsin.
[x] tailwindcss dokümantasyonunda "get started" bölümündeki ilk adım yapıldı. 2. ve 3. adımı yaparak kurulumu tamamlayabilirsin.

Sana düşen sadece Task.jsx component'indeki dönüşümü yapmak:
[x] Task.jsxcomponent'inde kullanılan task.css dosyasına bakarak oradaki class'ları tailwind class'ları ile yazabilirsin. Renkleri css'de geçtiği şekilde kullanmalısın. tailwind class'ları eğer istediğin değeri sağlamıyorsa, arbitrary olarak yazabilirsin( bg-[#ccc] v.b)
[x] İhtiyaç kalmadığında task.css ve reset.css dosyalarını import eden satırları silmelisin.
[x] css dosyasındaki .urgent ve .normal renkleri sürekli kullanılacağı için bunu config dosyasında theme altında aynı isimde(normal, urgent) custom renkler olarak tanımlaman isteniyor.
[ ] component içindeki deadline'lar direk data'dan gelen değeri yazıyor. date-fns kütüphanesindeki metodları kullanarak "1 gün sonra", "4 gün kaldı" gibi metin halinde yazman isteniyor.
[ ] eğer deadline'a 3 günden az kaldı ise deadline metninin arka planı custom tanımladığın urgent rengini, 3 günden fazla var ise normal değerini kullanmalı.

İpucu: dokümantasyonda customizing your theme bölümüne bakabilirsin.
İpucu: formatDistanceToNow ve differenceInDays metodları işine yarayabilir.
Önemli Not: dosyaadi.config.js gibi ayar dosyalarını güncellediğimizde, sunucuyu durdurup, yeniden çalıştırmak gerekir. Bunun için terminalde ctrl (ya da cmd) ve c tuşlarına aynı anda basarak sunucuyu durdurun. Sonra npm install && npm run wit yazın ve entera basın.
Çalışma dosyaları: src/components/Task.jsx, tailwind.config.js, index.css
