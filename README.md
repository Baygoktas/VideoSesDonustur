# Nedir bu bot?
Ac3 veya eac3 ses formatıyla kodlanmış yani telegramın destek vermediği hiç sesi olmayan Telegram videolarının sesini ffmpeg aracılığıyla acc formatına dönüştürüp sesin gelmesini sağlar ve bunu herhangi bir kalite kaybı olmadan yapar.

Çalışan bir örnek: [Video Sesini Dönüştür](https://t.me/SesVideoBot)

### Ortam Değişkenleri
Ortam değişkenlerine değerler ekleyin veya bunları [config.env](./config.env) içine ekleyin.
- `API_ID` - [https://my.telegram.org](https://my.telegram.org)'da bir uygulama oluşturarak edinin.
- `API_HASH` - [https://my.telegram.org](https://my.telegram.org)'da bir uygulama oluşturarak edinin.
- `BOT_TOKEN` - [https://t.me/BotFather](https://t.me/BotFather) adresinden bir bot oluşturarak edinin.
- `SUDO_USERS` - Yetkili kullanıcının ID numarasını ekleyin. Birden fazla kullanıcı için ayırıcı olarak boşuk kullanın.
- `DOWNLOAD_DIR` - (İsteğe bağlı) İndirilen dosyaları saklamak için geçici indirme dizini. Varsayılan 'indirilenler/'

### Kodlama Biçimini Yapılandırma
ffmpeg profilini değiştirmek istiyorsanız bunları şurada düzenleyin: [ffmpeg_utils.py](/bot/helper/ffmpeg_utils.py)

## Kolay Kurulum:
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Docker İle Kurulum:
```
# 1. Python ve Docker'ı kurun.

sudo snap install docker
sudo apt install python3

# 2. Repo'yu Klonlayın.

git clone https://github.com/Turkce-Botlar-Sohbet/VideoSesDonustur
cd VideoSesDonustur

# 3. Yapılandırma Dosyasını Ayarlayın.

nano config.env

# 4. Docker Görüntüsü Oluşturun.

sudo docker build . -t videosesdonustur

# 5. Botu Çalıştırın.

sudo docker run videosesdonustur
```

### Kurulum Gereksinimleri
Makinenize gerekli Python Modüllerini kurun.
```sh
apt-get -qq install ffmpeg
pip3 install -r requirements.txt
```
### Dağıtma
Python3.7 veya üstü ile.
```sh
python3 -m bot
```
