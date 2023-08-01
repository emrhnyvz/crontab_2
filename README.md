# crontab_2

Linux'da bir shell scripti crontab ile otomatik olarak çalıştırabilirsiniz İşte nasıl yapılacağını açıklayan bir örnektir
Terminali açın ve crontab'ı düzenlemek için aşağıdaki komutu kullanın
crontab -e
Bu, crontab dosyanızı açar (eğer daha önce hiç açmadıysanız, hangi editörü kullanmak istediğinizi sorar). Ardından, shell script'inizi ne zaman çalıştırmak istediğinizi belirtmek için bir cron işi (job) ekleyin.
Örneğin, her gün saat 2'de my_script.sh adlı bir shell scripti çalıştırmak istiyorsanız, crontab dosyanıza aşağıdaki satırı ekleyin:
0 2 * * * /path/to/your/script/my_script.sh
Bu satırın anlamı:

0 2 * * * her günün 2:00'inde (24 saat formatında) komutu çalıştır.
/path/to/your/script/my_script.sh burası komutunuzun tam yoludur. Burayı kendi script'inizin yoluna göre değiştirmelisiniz.
Dosyayı kaydedin ve kapatın. Bu, crontab'a yeni işinizi ekler ve belirttiğiniz zamanda çalıştırılmasını sağlar.
Not: Komutunuzun çalışabilmesi için shell script'inizin çalıştırılabilir olması gerekiyor. Bu işlemi aşağıdaki komut ile yapabilirsiniz:
chmod +x /path/to/your/script/my_script.sh
Ayrıca, crontab tarafından çalıştırılan işlerin çevresel yol ayarları standart ayarlardan farklı olabilir, bu yüzden scriptinizin içindeki tüm komutların tam yolunu belirtmeniz gerekebilir.
