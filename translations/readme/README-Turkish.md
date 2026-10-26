<h1 align="center">Auto PY to EXE</h1>
<p align="center">Python'da basit bir grafik arayüzü ve <a href="https://pyinstaller.readthedocs.io/en/stable/index.html">PyInstaller</a> kullanan bir .py'den .exe'ye dönüştürücü.</p>

<p align="center">
    <img src="https://nitratine.net/posts/auto-py-to-exe/feature.png" alt="Boş arayüz">
</p>

<p align="center">
    <a href="https://pypi.org/project/auto-py-to-exe/"><img src="https://img.shields.io/pypi/v/auto-py-to-exe.svg" alt="PyPI Sürümü"></a>
    <a href="https://pypi.org/project/auto-py-to-exe/"><img src="https://img.shields.io/pypi/pyversions/auto-py-to-exe.svg" alt="PyPI Desteklenen Sürümler"></a>
    <a href="https://pypi.org/project/auto-py-to-exe/"><img src="https://img.shields.io/pypi/l/auto-py-to-exe.svg" alt="Lisans"></a>
    <a href="https://pepy.tech/project/auto-py-to-exe"><img src="https://static.pepy.tech/badge/auto-py-to-exe/month" alt="Aylık İndirme"></a>
    <a href="https://pyinstaller.readthedocs.io/en/stable/requirements.html"><img src="https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20macos-lightgrey" alt="Desteklenen Platformlar"></a>
    <a href="https://www.buymeacoffee.com/brentvollebregt"><img src="https://img.shields.io/badge/-buy_me_a%C2%A0beer-gray?logo=buy-me-a-coffee" alt="Bağış Yap"></a>
</p>

[English](../../README.md)
| [简体中文](./README-Chinese_Simplified.md)
| [Suomen kieli](./README-Finnish.md)
| **Türkçe**
| [فارسی](./README-Persian.md)
| [한국어](./README-Korean.md)
| [Български](./README-Bulgarian.md)
| [हिन्दी](./README-Hindi.md)
| [עברית](./README-Hebrew.md)
| [العربية](./README-Arabic.md)
| [Беларуская](./README-Belarusian.md)
| [Slovenščina](./README-Slovenian.md)
| [српски](./README-Serbian_Cyrillic.md)
| [srpski](./README-Serbian_Latin.md)
| [Русский](./README-Russian.md)
| [Français](./README-French.md)

## Demo

<p align="center">
    <img src="https://nitratine.net/posts/auto-py-to-exe/auto-py-to-exe-demo.gif" alt="auto-py-to-exe Demo">
</p>

## Başlarken

### Gereksinimler

- Python: 3.6-3.14

_Görsellerde gösterilen arayüze sahip olmak için Chrome'a ihtiyacınız olacaktır. Chrome yüklü değilse veya `--default-browser` argümanı verilirse varsayılan tarayıcı kullanılacaktır._

### Kurulum ve Kullanım

#### [PyPI](https://pypi.org/project/auto-py-to-exe/) Üzerinden Kurulum

Bu projeyi PyPI kullanarak kurabilirsiniz:

```
pip install auto-py-to-exe
```

Ardından çalıştırmak için terminalde şu komutu yürütün:

```
auto-py-to-exe
```

> Bilgisayarınızda birden fazla Python sürümü yüklüyse `auto-py-to-exe` yerine `python -m auto_py_to_exe` komutunu kullanabilirsiniz.

#### [GitHub](https://github.com/brentvollebregt/auto-py-to-exe) Üzerinden Kurulum

```
git clone https://github.com/brentvollebregt/auto-py-to-exe.git
cd auto-py-to-exe
python setup.py install
```

Ardından çalıştırmak için terminalde şu komutu yürütün:

```
auto-py-to-exe
```

#### [GitHub](https://github.com/brentvollebregt/auto-py-to-exe) Üzerinden Yerel Olarak Çalıştırma (Kurulumsuz)

Aşağıdaki adımları izleyerek bu projeyi yerel olarak çalıştırabilirsiniz:

1. [Depoyu (repo)](https://github.com/brentvollebregt/auto-py-to-exe) klonlayın/indirin
2. Komut istemini (cmd)/terminali açın ve `cd` komutuyla projenin kök dizinine gidin
3. `python -m pip install -r requirements.txt` komutunu çalıştırın
4. Uygulamayı çalıştırmak için `python -m auto_py_to_exe` komutunu yürütün

## Uygulamayı Kullanma

1. Betik (script) konumunuzu seçin (yolu yapıştırın veya dosya gezginini kullanın)
   - Dosya mevcutsa dış çerçeve maviye dönecektir
2. Diğer seçenekleri belirleyin ve simge (icon) veya diğer dosyalar gibi öğeleri ekleyin
3. Dönüştürmek için alttaki büyük mavi düğmeye tıklayın
4. Tamamlandığında dönüştürülmüş dosyalarınızı `/output` dizininde bulabilirsiniz

_İşte bu kadar kolay._

### Argümanlar

Kullanım bilgisini almak için yardım bayrağını kullanın: `auto-py-to-exe --help`

| Argüman                                                      | Tür                  | Açıklama                                                                                                                                      |
| ------------------------------------------------------------ | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| filename                                                     | konumsal/isteğe bağlı| Arayüzdeki "Script Location" (Betik Konumu) alanını önceden doldurur.                                                                          |
| -db, --default-browser                                       | isteğe bağlı         | Arayüzü varsayılan tarayıcıyı (Chrome olabilir) kullanarak açar. Chrome'u bulmaya çalışmaz.                                                   |
| -nu, --no-ui                                                 | isteğe bağlı         | Arayüzü bir tarayıcıda açmaya çalışmaz ve yalnızca uygulamanın erişilebileceği adresi ekrana yazdırır.                                        |
| -c [CONFIG], --config [CONFIG]                               | isteğe bağlı         | Arayüzü önceden doldurmak için bir yapılandırma dosyası (JSON) sağlar. Bu dosyalar ayarlar sekmesinden oluşturulabilir.                       |
| -o [PATH], --output-dir [PATH]                               | isteğe bağlı         | Varsayılan çıktı dizinini ayarlar. Bu ayar yine de arayüzden değiştirilebilir.                                                                |
| -bdo [FOLDER_PATH], --build-directory-override [FOLDER_PATH] | isteğe bağlı         | Varsayılan derleme (build) dizinini geçersiz kılar. Antivirüsünüzün dosyaları silmesini önlemek için bir klasörü beyaz listeye almanız gerektiğinde kullanışlıdır. |
| -lang [LANGUAGE_CODE], --language [LANGUAGE_CODE]            | isteğe bağlı         | Arayüze açılırken hangi dili varsayılan olarak kullanması gerektiğini belirtir. Dil kodları aşağıdaki "Çeviriler" başlığı altındaki tabloda bulunabilir. |

### JSON Yapılandırması

Aynı verileri arayüze tekrar tekrar girmek yerine, ayarlar sekmesindeki "Configuration" (Yapılandırma) bölümüne gidip mevcut durumu bir JSON dosyasına dışa aktarabilirsiniz. Daha sonra tüm alanları yeniden doldurmak için bu dosyayı tekrar arayüze içe aktarabilirsiniz.

Bu JSON yapılandırmasını dışa aktarma işlemi, farklı bilgisayarlara taşındığında dizin yapıları değişebileceği için çıktı dizinini otomatik olarak kaydetmez. Çıktı dizininin JSON yapılandırmasında yer almasını istiyorsanız, JSON dosyasındaki `nonPyinstallerOptions.outputDirectory` altına dizini ekleyin (yeni bir anahtar oluşturmanız gerekecektir).

## Örnekler

[examples/](../../examples/) dizini, betiklerinizi nasıl yazacağınıza ve bunları auto-py-to-exe ile nasıl paketleyeceğinize dair bazı örnekler sunar.

- [Temel (konsol uygulaması)](../../examples/1-basic/readme.md)
- [Konsolsuz (genellikle GUI tabanlı uygulamalar için istendiği gibi)](../../examples/2-no-console/readme.md)
- [Görseller ve .py dışındaki diğer dosyalar (dahil edilecek statik dosyalar)](../../examples/3-images-and-other-non-py-files/readme.md)
- [Kalıcı veriler (veritabanları gibi)](../../examples/4-persistent-data/readme.md)

## Video

Başlarken görsel bir kaynağa ihtiyacınız varsa, [bu projenin ilk sürümü için hazırladığım videoyu](https://youtu.be/OZSZHmWSOeM) izleyebilirsiniz; bazı şeyler değişmiş olabilir ancak aynı temel kavramlar hâlâ geçerlidir.

## Katkıda Bulunma

Nasıl katkıda bulunabileceğinize dair yönergeleri görmek için [CONTRIBUTING.md](../../CONTRIBUTING.md) dosyasına göz atın. Bu dosya; yeni bir özelliğiniz, bir değişikliğiniz, çeviri güncellemeniz olduğunda veya auto-py-to-exe ile ilgili bir sorun bulduğunuzda ne yapmanız gerektiğini özetler.

## Aracı Kullanırken Karşılaşılan Sorunlar

Paketlenmiş çalıştırılabilir dosya (executable) ile veya genel olarak bu aracı kullanırken sorun yaşıyorsanız, [auto-py-to-exe kullanırken sık karşılaşılan sorunlar hakkındaki blog yazımı](https://nitratine.net/blog/post/issues-when-using-auto-py-to-exe/?utm_source=auto_py_to_exe&utm_medium=readme_link&utm_campaign=auto_py_to_exe_help) okumanızı tavsiye ederim. Bu yazı, Python betiklerini paketleme hakkında bilmeniz gerekenleri ve sıkça ters giden durumlar için çözümleri kapsar.

Bu araçla ilgili bir hata bulduğunuza inanıyorsanız, lütfen [CONTRIBUTING.md dosyasındaki "Reporting an Issue" (Sorun Bildirme) bölümünü](../../CONTRIBUTING.md#reporting-an-issue) takip edin.

## Çeviriler

| Dil                                         | Çevirmenler                                                                                  | Arayüz (UI)            | README                                           | CONTRIBUTING                                                 | Örnekler |
| ------------------------------------------- | -------------------------------------------------------------------------------------------- | ---------------------- | ------------------------------------------------ | ------------------------------------------------------------ | -------- |
| Arabic (العربية)                            | [Tayeb-Ali](https://github.com/tayeb-ali), [0xTrix](https://github.com/0xTrix)               | ✔️                     | [✔️](./README-Arabic.md)                         |                                                              |          |
| Belarusian (Беларуская)                     | [Zmicier21](https://github.com/Zmicier21)                                                    | ✔️[⚠️](# 'Eksik')      | [✔️](./README-Belarusian.md)                     |                                                              |          |
| Brazilian Portuguese (Português Brasileiro) | [marleyas](https://github.com/marleyas), [reneoliveirajr](https://github.com/reneoliveirajr) | ✔️                     |                                                  |                                                              |          |
| Bulgarian (Български)                       | [kbkozlev](https://github.com/kbkozlev)                                                      | ✔️                     | [✔️](./README-Bulgarian.md)                      |                                                              |          |
| Chinese Simplified (简体中文)               | [jiangzhe11](https://github.com/jiangzhe11), [Emptylight](https://github.com/emptylight370)  | ✔️                     | [✔️](./README-Chinese_Simplified.md)             | [✔️](../contributing/CONTRIBUTING-Chinese_Simplified.md)     |          |
| Chinese Traditional (繁體中文)              | [startgo](https://github.com/ystartgo)                                                       | ✔️                     |                                                  |                                                              |          |
| Czech (Čeština)                             | [Matto58](https://github.com/Matto58)                                                        | ✔️                     |                                                  |                                                              |          |
| Dutch (Nederlands)                          | [barremans](https://github.com/barremans)                                                    | ✔️                     |                                                  |                                                              |          |
| English                                     | -                                                                                            | ✔️                     | ✔️                                               | ✔️                                                           | ✔️       |
| Finnish (Suomen kieli)                      | [ZapX5](https://github.com/ZapX5)                                                            | ✔️                     | [✔️](./README-Finnish.md)                        |                                                              |          |
| French (Français)                           | [flaviedesp](https://github.com/flaviedesp), [samuellouf](https://github.com/samuellouf)     | ✔️                     | [✔️](./README-French.md)                         |                                                              |          |
| German (Deutsch)                            | [hebens](https://github.com/hebens), [ackhh](https://github.com/ackhh)                       | ✔️                     |                                                  |                                                              |          |
| Greek (Ελληνικά)                            | [sofronas](https://github.com/sofronas)                                                      | ✔️                     |                                                  |                                                              |          |
| Hebrew (עברית)                              | [ronbentata](https://github.com/ronbentata)                                                  | ✔️                     | [✔️](./README-Hebrew.md)                         |                                                              |          |
| Hindi (हिन्दी)                              | [triach-rold](https://github.com/triach-rold)                                                | ✔️                     | [✔️](./README-Hindi.md)                          |                                                              |          |
| Hungarian (Magyar)                          | [synexdev01](https://github.com/synexdev01)                                                  | ✔️                     |                                                  |                                                              |          |
| Indonesian (Bahasa Indonesia)               | [MarvinZhong](https://github.com/MarvinZhong)                                                | ✔️                     |                                                  |                                                              |          |
| Italian (Italiano)                          | [itsEmax64](https://github.com/itsEmax64)                                                    | ✔️                     |                                                  |                                                              |          |
| Japanese (日本語)                           | [NattyanTV](https://github.com/nattyan-tv)                                                   | ✔️                     |                                                  |                                                              |          |
| Korean (한국어)                             | [jhk1090](https://github.com/jhk1090)                                                        | ✔️                     | [✔️](./README-Korean.md)                         |                                                              |          |
| Persian (فارسی)                             | [DrunkLeen](https://github.com/drunkleen), [Ar.dst](https://github.com/Ar-dst)               | ✔️                     | [✔️](./README-Persian.md)                        |                                                              |          |
| Polish (Polski)                             | [Akuczaku](https://github.com/Akuczaku)                                                      | ✔️                     |                                                  |                                                              |          |
| Russian (Русский)                           | Oleg, [Sandile](https://github.com/Sandile225325)                                            | ✔️                     | [✔️](./README-Russian.md)                        |                                                              |          |
| Serbian Cyrillic (српски)                   | [Radoš Milićev](https://github.com/rammba)                                                   | ✔️                     | [✔️](./README-Serbian_Cyrillic.md)               | [✔️](../contributing/CONTRIBUTING-Serbian_Cyrillic.md)       | ✔️       |
| Serbian Latin (srpski)                      | [rina](https://github.com/sweatshirts), [Radoš Milićev](https://github.com/rammba)           | ✔️                     | [✔️](./README-Serbian_Latin.md)                  | [✔️](../contributing/CONTRIBUTING-Serbian_Latin.md)          | ✔️       |
| Slovak (Slovenčina)                         | [mostypc123](https://github.com/mostypc123)                                                  | ✔️                     |                                                  |                                                              |          |
| Slovenian (Slovenščina)                     | [Andrew Poženel](https://github.com/anderlli0053)                                            | ✔️                     | [✔️](./README-Slovenian.md)                      |                                                              |          |
| Spanish (Español)                           | [enriiquee](https://github.com/enriiquee)                                                    | ✔️                     |                                                  |                                                              |          |
| Spanish Latin America (Español Latam)       | [Matyrela](https://github.com/Matyrela)                                                      | ✔️                     |                                                  |                                                              |          |
| Thai (ภาษาไทย)                              | [teerut26](https://github.com/teerut26)                                                      | ✔️[⚠️](# 'Eksik')      |                                                  |                                                              |          |
| Turkish (Türkçe)                            | [mcagriaksoy](https://github.com/mcagriaksoy), [MustafaKoca](https://github.com/MustafaKoca9) | ✔️            | [✔️](./README-Turkish.md)                        |                                                              |          |
| Ukrainian (Українська)                      | [AndrejGorodnij](https://github.com/AndrejGorodnij)                                          | ✔️                     |                                                  |                                                              |          |
| Vietnamese (Tiếng Việt)                     | [7777Hecker](https://github.com/7777Hecker)                                                  | ✔️                     |                                                  |                                                              |          |

> Başka bir dil için çeviri eklemek ister misiniz? [CONTRIBUTING.md dosyasındaki "Add or Update a Translation" (Çeviri Ekleme veya Güncelleme) bölümünü](../../CONTRIBUTING.md#add-or-update-a-translation) takip edin.

## Python 2.7 Desteği

9 Ağustos 2020'de yayınlanan [PyInstaller v4.0](https://github.com/pyinstaller/pyinstaller/releases/tag/v4.0) itibarıyla Python 2.7 artık desteklenmemektedir; ancak PyInstaller'ın daha eski bir sürümünü kurarak bu aracı Python 2.7 ile kullanmaya devam edebilirsiniz. [PyInstaller v3.6](https://github.com/pyinstaller/pyinstaller/releases/tag/v3.6), Python 2.7'yi destekleyen son sürümdü; bunu kurmak için önce mevcut PyInstaller sürümlerini kaldırın ve ardından `python -m pip install pyinstaller==3.6` komutunu çalıştırın.

## Test Etme

Testler [tests/](../../tests/) dizininde bulunur ve pytest kullanılarak çalıştırılır:

```
pip install pytest
pip install -e .
pytest
```

## Ekran Görüntüleri

| <!-- -->                                                                                                                                             | <!-- -->                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| [![Boş arayüz](https://nitratine.net/posts/auto-py-to-exe/empty-interface.png)](https://nitratine.net/posts/auto-py-to-exe/empty-interface.png)      | [![Doldurulmuş](https://nitratine.net/posts/auto-py-to-exe/filled-out.png)](https://nitratine.net/posts/auto-py-to-exe/filled-out.png) |
| [![Dönüştürülüyor](https://nitratine.net/posts/auto-py-to-exe/converting.png)](https://nitratine.net/posts/auto-py-to-exe/converting.png)            | [![Tamamlandı](https://nitratine.net/posts/auto-py-to-exe/completed.png)](https://nitratine.net/posts/auto-py-to-exe/completed.png)    |
