# Friend Field — FL Studio `.flp` и `.mid`

Джазовый кроссовер на основе **`Garden of Hopes and Dreams`** (`Garden of hnd.mid`, `125.0 BPM`, `4/4`, `106` тактов = `3:23.52`) с заменой лейтмотивов и полным переносом на инструменты и микшер из **`Field of Hopes and Dreams`** (`Field of hnd.flp`).

---

## Файлы результата в папке `Friend Field/`

- **`Friend Field/Friend Field.flp`** — готовый проект FL Studio (`125.0 BPM`, `56` именованных паттернов, `69` клипов на Playlist, все инструменты и эффекты микшера из `Field of hnd.flp`).
- **`Friend Field/Friend Field.mid`** — итоговый MIDI-файл (`15` дорожек, `7 427` нот, `3:23.52`) со всеми заменёнными лейтмотивами.

---

## Структура трека и замены лейтмотивов

1. **0:00 – 0:34 (Такты 1–18, Вступление — играет один раз при первом входе в Сад):**
   - `0:00 – 0:07` (такты 1–4): вступительное пианино `piano intro` + лёгкий звон `music box`.
   - `0:07 – 0:19` (такты 5–10): вместо *Once Upon a Time* аккуратно вплетена первая часть **`Don't Forget`** (`Don't forget motif.mid`, перенесена в **Bb major / G minor** в том же разрежённом атмосферном стиле: флейта/белл `triangle` + саксофон `blow tenor` + хор/брасс `choir ahhs` + `celesta` переливы + `piano intro`).
   - `0:19 – 0:34` (такты 11–18): классическое вступление *Field of Hopes and Dreams* + реверс-разгон `FLS Crash 01b` к 19-му такту.
2. **0:34 – 1:12 (Такты 19–42, Основная тема — ТОЧКА СТАРТА ЦИКЛА):**
   - Основная джазовая тема *Field of Hopes and Dreams* (`slap bass + saw`, `piano`, `power` drums, `violin`, `pizzicato strings`, `choir ahhs`).
3. **1:12 – 1:55 (Такты 43–60, Кульминация и соло):**
   - На тактах 43–50 оригинальный *Don't Forget* заменён на тему **`Tale`** (упрощённая вторая часть *Once Upon a Time* в **Bb major** с мягкой гармонизацией `Eb -> F -> Db6 -> Gm`).
   - На тактах 51–56 тема **`Tale`** звучит в диалоге с фирменной **джазовой партией тенор-саксофона Карлоса Эйена** (`blow tenor`), переходя в пик соло на тактах 57–60.
4. **1:55 – 2:29 (Такты 61–78, Импровизационный бридж):**
   - Оригинальный джазовый бридж (`blow tenor + tyros nylon`, `piano`, `celesta`, `music box`, `choir ahhs`, `power`).
5. **2:29 – 2:37 (Такты 79–86, Возвращение темы):**
   - Короткий рефрен *Field of Hopes and Dreams* + разгон в финал.
6. **2:37 – 3:11 (Такты 87–98, Финальное развитие):**
   - Мощное октавное проведение лейтмотива **`Tale`** (такты 87–92: `triangle` + `celesta` + `blow tenor` + `violin` + `choir ahhs`), переходящее в закрывающий рифф тактов 93–98.
7. **3:11 – 3:23 (Такты 99–106, Завершение и выход на цикл):**
   - Плавное затухание на `piano intro` + `music box` и точный возврат к такту **19 (`0:34.56`)**.

---

## Использованные инструменты из `Field of hnd.flp`

- **Строй исправлен:** у каналов `CH 01..13` в исходном `Field of hnd.flp` стоял `pitch_shift = -200`; в `Friend Field.flp` он сброшен в **`0`** на всех каналах, чтобы все партии звучали строго в строе A=440 Гц.
- **Референс (`CH 00`):** исходный OST-трек отвязан и заглушен, чтобы FL Studio не показывал ошибку поиска файла.
- **SoundFont-ы и встроенные плагины `Field of hnd.flp`:**
  - `SGM-V2.01.sf2`: `power` (Patch 145), `slap bass` (Patch 38), `choir ahhs` (Patch 53), `violin` (Patch 41), `pizzicato strings` (Patch 46), `piano intro` (Patch 1), `piano` (Patch 1)
  - `THInst.sf2`: `celesta` (Patch 9), `music box` (Patch 11), `blow tenor` (Patch 67), `tyros nylon` (Patch 25)
  - Встроенные FL Studio: `3x Osc` (`triangle`, `saw`), `FLS Crash 01b` (Reverse), `FLS Crash 02a`
  - Эффекты микшера шаблона `Field of hnd.flp`: встроенные `Maximus`, `Fruity Limiter`, `Fruity Parametric EQ 2`, `Fruity Delay 2`, `Fruity Stereo Shaper`, плюс сторонние из оригинального шаблона (`Fruity Reeverb`, `Bertom_PhantomCenter`, `FabFilter Pro-Q 3` на `ref/master` — если какого-то стороннего плагина нет, при открытии нажмите OK, всё остальное загрузится штатно).

---

## Как поставить точку зацикливания на 0:34 (Такт 19) в FL Studio

1. Откройте `Friend Field/Friend Field.flp` в FL Studio.
2. Поставьте курсор Playlist ровно на начало **такта 19** (`0:34.56`, там начинается паттерн **`Main Theme LOOP (0:34)`**).
3. Нажмите **`Alt + T`** (Add Time Marker), назовите метку например `Loop`, затем нажмите на неё правой кнопкой мыши и выберите **`Loop`** — тогда FL Studio проиграет `0:00–0:34` ровно один раз и дальше будет бесконечно крутить основную часть `0:34–3:23`.
4. Для экспорта в игру лучше всего выгрузить **2 отдельных WAV/OGG файла** из `Friend Field.flp`:
   - `friend_field_intro.ogg` — выделите на линейке Playlist ровно **такты 1–19** (`0:00 – 0:34.56`, `Tail: Cut remainder`)
   - `friend_field_loop.ogg` — выделите **такты 19–107** (`0:34.56 – 3:23.52`, `Tail: Wrap remainder`)
