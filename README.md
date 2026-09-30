<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0b1220,100:0e7490&height=110&section=header&text=Announcer&fontSize=42&fontColor=22d3ee&fontAlignY=54&desc=Scheduled%20and%20instant%20announcements&descSize=13&descColor=94a3b8&descAlignY=80" width="100%" alt="Announcer" />

<p>
<img src="https://img.shields.io/github/v/release/chizzar-dev/Announcer?style=flat&label=release&color=06b6d4&labelColor=0b1220" alt="release" />
<img src="https://img.shields.io/badge/Minecraft-1.8%20%E2%80%93%201.21.11-0891b2?style=flat&labelColor=0b1220" alt="Minecraft 1.8 - 1.21.11" />
<img src="https://img.shields.io/badge/Java-8%2B-155e75?style=flat&labelColor=0b1220&logo=openjdk&logoColor=22d3ee" alt="Java 8+" />
<a href="LICENSE"><img src="https://img.shields.io/github/license/chizzar-dev/Announcer?style=flat&label=license&color=0e7490&labelColor=0b1220" alt="license" /></a>
</p>

</div>

Announcer posts automatic chat announcements at an interval and lets staff send an instant center-screen broadcast.

*Announcer, belirli araliklarla otomatik sohbet duyurulari gonderir ve yetkililerin ekran ortasinda anlik duyuru yapmasina izin verir.*

## Features · Özellikler
- Ayarlanabilir süre aralığı (saniye)
- Sıralı veya rastgele gönderim
- Çok satırlı duyuru desteği + özelleştirilebilir prefix
- **`/duyuru <mesaj>`** → herkese ekran ortasında title duyuru (`Yetkili : mesaj`)
- Duyuru etiketi (`Yetkili`) ve renkler configden ayarlanabilir

## Installation · Kurulum
1. `Announcer.jar` dosyasını [Releases](https://github.com/chizzar-dev/Announcer/releases/latest) sayfasından indir.
2. Sunucunun `plugins/` klasörüne at.
3. Sunucuyu yeniden başlat.
4. `plugins/Announcer/config.yml` dosyasından duyuruları düzenle.

## Commands · Komutlar
| Komut | Açıklama | Yetki |
|-------|----------|-------|
| `/duyuru <mesaj>` | Ekran ortasında anlık duyuru gönderir | `announcer.say` |
| `/announcer reload` | Configi yeniden yükler | `announcer.admin` |
| `/announcer next` | Sıradaki otomatik duyuruyu hemen gönderir | `announcer.admin` |

**Alias:** `/duyuru` · `/ac`

## Permissions · Yetkiler
| Yetki | Açıklama | Varsayılan |
|-------|----------|------------|
| `announcer.say` | `/duyuru <mesaj>` ile anlık duyuru atar | op |
| `announcer.admin` | reload ve next | op |

## Configuration · Ayarlar
| Anahtar | Açıklama |
|---------|----------|
| `announcer.interval` | Otomatik duyurular arası süre (saniye) |
| `announcer.random` | `true` = rastgele, `false` = sırayla |
| `announcer.prefix` | Otomatik duyuruların başına eklenir |
| `announcer.messages` | Duyuru listesi (her biri bir/birden çok satır) |
| `announcer.say.title` | `/duyuru` üst satır etiketi (`Yetkili`) |
| `announcer.say.subtitle` | `/duyuru` alt satır (`%message%`) |
| `announcer.say.fade-in/stay/fade-out` | Title süreleri (tick) |

`%player%` (gönderen) ve `%message%` (yazılan mesaj) yer tutucuları `say` içinde kullanılabilir.

## Building · Derleme
```bash
mvn clean package
```
Çıktı · Output: `target/Announcer.jar`

Her push [GitHub Actions](https://github.com/chizzar-dev/Announcer/actions/workflows/build.yml) ile derlenir; `v*` etiketli sürümler jar'la birlikte [Releases](https://github.com/chizzar-dev/Announcer/releases) sayfasına eklenir.
<br><sub>Every push is built by GitHub Actions; tagged `v*` releases attach the jar.</sub>

## License · Lisans
[MIT](LICENSE) — istediğin gibi kullan, değiştir, dağıt · use, modify and distribute freely

<div align="center"><sub>chizzar-dev · Minecraft plugins for 1.8 – 1.21.11 · <a href="https://discord.gg/forges">Discord</a></sub></div>
