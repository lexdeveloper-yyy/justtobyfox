# Scarlet Sun

**«Scarlet Sun»** — кроссовер-аранжировка, объединяющая все оригинальные лейтмотивы композиции *Sunset of Seven Suns* (`sunset of the seven suns.flp`) с барочно-маршевой гармонией, тональностью `F# minor / A major` (`120.0 BPM`, `4/4`, `PPQ = 96`, `64 такта`) и оркестровым тембром *Scarlet Forest* (`19. scarlet forest.flp`).

---

## Состав релиза (2 готовых FLP-проекта + MIDI)

Проект собран в двух полностью независимых вариантах с чистым встроенным микшером FL Studio (**0 сторонних VST / `Fruity Wrapper`**) и с нуля перенесён в FLP по проверенному пайплайну **`.mid` -> именованные паттерны FLP**:

1. **`Scarlet Sun/Scarlet Sun.flp`** — **Вариант 1 (оригинальный оркестровый темплейт *Scarlet Forest*)**
   - `19` каналов (`CH 01..18` активны: `squidfont_orchestral.sf2`, `THInst.sf2`, `SGM-V2.01.sf2`, `specifically toby\glockenspiel.sf2`; `CH 00` отвязан и замьючен без референсного аудиофайла).
   - `50` именованных паттернов (`New`, `Name`, `Notes`), `50` клипов плейлиста (`Track 2..8`), `4 627` нот.
   - Оригинальная маршрутизация и эффекты микшера *Scarlet Forest* с заменой сторонних VST-слотов (`FabFilter Pro-Q 3`, `Bertom_PhantomCenter`, `Fruity Reeverb.dll`) на встроенные плагины FL Studio (`Fruity Parametric EQ 2`, `Fruity Convolver`, `Fruity Delay 2`, `Fruity Stereo Enhancer`, `Fruity Limiter`).

2. **`Scarlet Sun/Scarlet Sun (Universal).zip`** *(и распакованная папка `Scarlet Sun/Scarlet Sun (Universal)/`)* — **Вариант 2 (универсальный Zipped Loop Package)**
   - Не требует `squidfont_orchestral.sf2`, `glockenspiel.sf2` и никаких сторонних VST-плагинов: работает на стандартных звуках **`SGM-V2.01.sf2`** + **`THInst.sf2`** (`celesta`, `th pizz`, `th oboe`, `th strings`) + встроенном микшере FL Studio.
   - Включает `23` канала (`4 859` нот): дополнительно добавлены аутентичные партии **`shamisen`** (`SGM p107`) и **`pan flute`** (`SGM p76`), а также живые удары тарелок **`FLS Crash 02a.wav` / `FLS Crash 02b.wav`** из *Sunset of Seven Suns* (ударные перемаплены на GM *Power Kit* `p145` с `pitch_shift = 0`).
   - Внутрь архива `.zip` упакованы сам `.flp` и все локальные WAV/WV-ресурсы (`FLS Crash 02a.wav`, `FLS Crash 02b.wav`, `IMP Evnt - Room Bright.wv`, `IMP Lex - Close Warm Room.wv`) — открывается в FL Studio напрямую через `File -> Open`.

3. **`Scarlet Sun/Scarlet Sun.mid`** — синхронизированный MIDI-файл (`19` треков, `4 627` нот, `120.0 BPM`, `PPQ = 96`).

---

## Что было исправлено по сравнению с первой версией

- **Восстановлено воспроизведение клипов в FL Studio:** убраны `NaN`-смещения клипов плейлиста (`0000c07f` -> корректные `-1.0` / `000080bf` на каждом из 50 клипов, `track_rvidx = 199 - track_iid`, `CurrentlySelected = 1`).
- **Перестроены паттерны по стандарту *Friend Field* / *Rude Buster*:** каждый из `50` паттернов имеет строго `3` события (`PatternID.New`, `PatternID.Name`, `PatternID.Notes`) и понятные имена по секциям и ролям (`Bass | 01 Intro A`, `Winds | 04A Drop A`, и т.д.).
- **Отвязан референс `CH 00`:** сняты `IsEnabled`, `IsLocked` и `SamplePath`, дорожка `Track 1` отключена.
- **Очищен микшер от сторонних VST:** все `Fruity Wrapper` слоты удалены и заменены на штатные эффекты FL Studio (`Fruity Convolver`, `Fruity Parametric EQ 2`, `Fruity Delay 2`, `Fruity Limiter`).
- **Вычищена гармоническая ткань и добавлены живые фразы *Sunset*:** устранены все диссонансы на малую секунду (`0` конфликтов в `4 627` нотах), расширен мелодический контрапункт деревянных духовых, оркестровых пиццикато и фортепианной коды.

---

## Структура аранжировки (B01–B64)

| Такты | Секция | Лейтмотив (*Sunset of Seven Suns* в `F#m`) и оркестровка |
| :--- | :--- | :--- |
| **B01–B08** | `01 Intro A` | **Лейтмотив 1A**: задумчивая тема на `th oboe` и `pan flute` поверх арпеджио `piano`, `clarinett staccato` / `shamisen`, мягкого баса `c bass + bassoon` и `celli pizz` |
| **B09–B16** | `02 Intro B` | **Лейтмотив 1B**: вступление смычковых (`vins legato`, `th strings`), парящая флейтово-гобойная линия на `oboe legato + th oboe (+ pan flute)` |
| **B17–B24** | `03 Pre-Drop A1` | **Лейтмотив 2 (1-е проведение)**: выход `bassoon stereo`, оркестровый напор струнных, барочный контрапункт и сбивка ударных в **B24** |
| **B25–B32** | `04A Drop A` | **Лейтмотив 2 (полный дроп)**: маршевый грув `kit`, офф-бит `bassoon stereo + celli pizz + th pizz`, искрящийся `piccalo staccato` и удары тарелок в **B25 / B29** |
| **B33–B40** | `04B Drop Climax` | **Кульминация дропа**: октавный взлёт струнных на `B34 / B38`, верхний контр-голос `oboe legato` и усиленная перкуссия |
| **B41–B48** | `05 Section B1` | **Лейтмотив 3**: кантиленные диалоги `oboe stac`, `clarinett staccato`, `piccalo staccato` и `glockenspiel / celesta` поверх фортепианных фигураций |
| **B49–B56** | `06 Section B2` | **Лейтмотив 4**: двухголосный дуэт `oboe legato + th oboe (+ pan flute)` с тёплым подкладом `th strings`, стоп-тайм и сбивка в **B56** |
| **B57–B64** | `07 Finale & Coda` | **Финальный триумф Главной темы** (`B57–B62`), оркестровая фермата на `C#7/F` в **B63** и прощальная сольная кода на `piano #2` (`Insert 11`) + `th oboe` в **B64** |

---

## Проверка качества (Automated Audits)

- `Track overlaps: 0` (нет пересечений клипов на дорожках плейлиста `Track 2..8`)
- `Note overlaps: 0` (нет наложений нот на одном канале и высоте)
- `Minor-2nd clashes (diff == 1): 0` (проверено по всем тактам и инструментам)
- `Playlist start_offset / end_offset`: `100%` клипов (`50/50`) в обоих проектах имеют точные байты `000080bf000080bf` (`-1.0 / -1.0`)
- `Fruity Wrapper (3rd-party VST) count`: `0` в обоих проектах (`Scarlet Sun.flp` и `Scarlet Sun (Universal).flp`)
