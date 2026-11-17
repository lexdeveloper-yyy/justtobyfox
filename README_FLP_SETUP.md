# Bird That Carries You Over A Disproportionately Small Gap — Rude Buster v4 Instruments (FL Studio `.flp`)

Проект перенесён с вашего `72`-тактового бесшовного MIDI (`160 BPM`, `4/4`, включая тему **Berdly** в `4/4` и все переходы) на инструменты и микшер из **`10. rude buster v4.zip` (`rude buster v4.flp`)** — **абсолютно без изменения самой мелодии, ритма, тональности и длительности нот**.

---

## Что внутри

1. **`35 Bird That Carries You Over A Disproportionately Small Gap (Rude Buster v4 Instruments).zip`**  
   Готовый **Zipped Loop Package** для FL Studio — внутри лежат сам `.flp` и все 3 WAV-сэмпла (`909 Crash.wav`, `Atmosphere Crash.wav`, `Funk Star Break.wav`).
2. **`flp_rude_buster_v4/`**  
   Распакованная папка с тем же проектом:
   - `35 Bird That Carries You Over A Disproportionately Small Gap (Rude Buster v4 Instruments).flp`
   - `909 Crash.wav`
   - `Atmosphere Crash.wav`
   - `Funk Star Break.wav`

---

## Точная проверка переноса (1-в-1 без изменения мелодии)

- **Темп:** ровно `160.0 BPM`, размер `4/4`, `PPQ = 96`.
- **Длина:** ровно `72` такта (`27 648` FL-тиков = `108.000` сек = `1:48.000`, бесшовный цикл).
- **Ноты MIDI:** перенесены все `4 033` ноты (`T0..T5`) с точностью до тика (`0` потерянных нот, `0` сдвигов высоты или длительности).
- **Pitch-фикс:** в оригинальном `rude buster v4.flp` у каналов `CH 01..08` стояли смещения высоты (`pitch_shift = 640` на пианино и `40` на остальных). Они сброшены в **`0`**, чтобы все ноты звучали в едином строе A=440 Гц.
- **Референс-дорожка (`ref`):** оригинальный `Toby Fox - Rude Buster.wav` отвязан и заглушен, чтобы FL Studio не ругался на отсутствующий OST-файл.

---

## Карта инструментов (из `rude buster v4.flp`)

| Дорожка Playlist | Каналы FL (`Channel Rack`) | Пресет / Сэмпл | Какую партию MIDI играет |
|---|---|---|---|
| `crashes` | `CH 09: 909 Crash` + `CH 10: Atmosphere Crash` | `909 Crash.wav` / `Atmosphere Crash.wav` (`Reverse`) | Акценты на дропах (`5, 9, 17, 25, 33, 41, 49, 57, 65, 69` такты) + реверс-разгоны перед ключевыми переходами |
| `funk star break(OMG)` | `CH 08: Funk Star Break` | `Fruity Slicer` (`Funk Star Break.wav`, авто-синк под `160 BPM`) | Ломаный брейкбит на драйвовых `4/4` секциях (выключается на интро `1–4`, бридже `41–48`, брейкдауне `49–52`, разгоне `56` и финальном вдохе `72`) |
| `genesis drums` | `CH 07: genesis kit` | `GenesiSF.SF2` (`Bank 128, Patch 000`) | Полная ударная партия `T5` (бочки, снейры, хэты, томы, крэши; тамбурин `54` -> Genesis Clap `39`, Crash 2 `57` -> Crash `49`) |
| `stupid pianos` | `CH 01: piano 1` + `CH 02: 000` | `SGM-V2.01.sf2` (`Patch 000`) + `pc98_ym2608.sf2` (`Patch 000`) | Ритм-аккорды `T1` + искрящиеся арпеджио/перезвоны `T3` в Припеве, Бридже, Брейкдауне и 67–68 тактах финала |
| `stupid bass` | `CH 03: 105 (crunchy bass)` + `CH 04: 082 (synth bass)` | `pc98_ym2608.sf2` (`Patch 105` + `Patch 082`) | Вся басовая линия `T0` с сочным FM-рыком и саб-плотностью |
| `love you lead <3` | `CH 06: 71 (lead)` + `CH 05: 084 (guitar)` | `pc98_ym2608.sf2` (`Patch 071` + `Patch 084`) | Главная мелодия `Bird` / `Berdly` / Припев (`T2`/`T3` на `71 lead` + октавный гитарный слой `T4` на `084 guitar`) |
| `what` | `CH 02: 000` | `pc98_ym2608.sf2` (`Patch 000`) | Контрапункт и подголоски `T2` в `Ch4b (Berdly)` и `Ch7 (Climax)` |

---

## Как открыть и настроить в нужном виде в FL Studio

### Шаг 1. Откройте проект вместе с WAV-сэмплами
- **Самый простой способ:** в FL Studio нажмите `File -> Open...` и выберите **`35 Bird That Carries You Over A Disproportionately Small Gap (Rude Buster v4 Instruments).zip`** (FL Studio сам распакует проект вместе с 3 WAV-файлами).
- **Альтернатива:** скопируйте папку **`flp_rude_buster_v4/`** целиком и откройте `.flp` внутри неё (главное — чтобы все 3 `.wav` лежали в той же папке рядом с `.flp`).

### Шаг 2. Проверьте SoundFont-банки (`.sf2`)
В шаблоне `rude buster v4.flp` (автор `@stormstudios1`) используются 3 SoundFont-файла, которые в самом архиве `10. rude buster v4.zip` не вшиты — FL Studio ищет их по путям шаблона:
- `%USERPROFILE%\Documents\music plugins\Soundfonts\UTDR\SGM-V2.01.sf2` -> для `CH 01 (piano 1)` (`Patch 000`)
- `%USERPROFILE%\Documents\music plugins\Soundfonts\UTDR\pc98_ym2608.sf2` -> для:
  - `CH 02 (000)` -> `Patch 000`
  - `CH 03 (105 crunchy bass)` -> `Patch 105`
  - `CH 04 (082 synth bass)` -> `Patch 082`
  - `CH 05 (084 guitar)` -> `Patch 084`
  - `CH 06 (71 lead)` -> `Patch 071`
- `%USERPROFILE%\Documents\music plugins\Soundfonts\GenesiSF.SF2` -> для `CH 07 (genesis kit)` (`Bank 128, Patch 000`)

**Как сделать без ручной перепривязки:**
1. Положите эти 3 `.sf2` в `Документы\music plugins\Soundfonts\` (как указано выше) **или**
2. Добавьте папку с вашими `.sf2` в `Options -> File settings -> Browser extra search folders`, чтобы FL Studio подхватил их автоматически.
3. Если вы открываете проект и один из каналов `Fruity Soundfont Player` пустой — нажмите на жёлтую иконку папки внутри плагина, выберите нужный `.sf2` и выставьте номер пресета (`Patch`) из таблицы выше. *(Если у вас FL Studio Trial/Fruity Edition и `Fruity Soundfont Player` в режиме демо, его можно заменить на встроенный **DirectWave** или бесплатный **Sforzando** / **JuicySFPlugin**, указав те же `.sf2` и номера патчей.)*

### Шаг 3. Что делать, если при открытии FL Studio ругается на плагины микшера
В оригинальном `rude buster v4.flp` в микшере стоят:
- На `Master`: **`Bertom_PhantomCenter`** (бесплатный VST3) + `Fruity Stereo Shaper` + `Fruity Limiter` + `Wave Candy`.
- На `Insert 1 (piano)`: `Fruity Delay 2` + старый VST **`Fruity Reeverb`**.

Если чего-то из сторонних плагинов нет на ПК:
- Нажмите **OK** в окне уведомления — вся музыка и остальные каналы загрузятся нормально.
- На `Insert 1 (piano)` при желании в пустой слот поставьте встроенный **`Fruity Reeverb 2`** (`Wet ~ 25–30%`), а на `Master` просто удалите отсутствующий слот `Bertom_PhantomCenter` (встроенные `Fruity Limiter` и `Fruity Stereo Shaper` останутся работать).

### Шаг 4. Быстрая доводка баланса под свой вкус (по желанию)
Весь проект аккуратно разделён по **7 дорожкам Playlist** и **47 именованным паттернам**, поэтому вы можете легко подстроить любой элемент:
- Если хочется чуть меньше брейкбита на куплетах `Ch2`/`Ch4`, просто уменьшите громкость `CH 08 (Funk Star Break)` в Channel Rack или замьютьте отдельные клипы на дорожке `funk star break(OMG)`.
- Если на `Ch3` / `Ch5` хочется ещё больше блеска от `piano 1`, слегка приоткройте громкость `Insert 1 (piano)`.
- Если бас на низких нотах `F1–A1` кажется слишком глубоким для ваших колонок, на `Insert` баса (можно направить `CH 03` и `CH 04` на свободный `Insert 5`) повесьте `Fruity Parametric EQ 2` с лёгким срезом ниже `35–40 Hz` и чуть поднимите `100–140 Hz`.

### Шаг 5. Как отрендерить готовый бесшовный цикл
1. Вверху включите режим **SONG** (не PAT) и убедитесь, что в Playlist выделения нет (или выделены ровно такты **`1–73`**, т.е. полные `72` такта).
2. Нажмите **`File -> Export -> WAV/MP3/OGG file...`**.
3. В окне рендера выставите:
   - **Mode:** `Full song`
   - **Tail:** **`Wrap remainder`** (это главное для бесшовного зацикливания — хвост реверберации/дилея с `72`-го такта перенесётся в самое начало `1`-го такта!).
   - Для игры/бесшовного лупа лучше сохранять в **`.ogg` или `.wav`** (у `.mp3` из-за кодека всегда добавляется крошечная пауза в начале файла).
