# Java Step Visualizer

🇬🇧 [English](#-english) &nbsp;|&nbsp; 🇹🇷 [Türkçe](#-türkçe)

---

## 🇬🇧 English

### 🔗 Live Demo
> **[▶ Open Java Step Visualizer (English)](https://canerztk8.github.io/java-step-visualizer/java-visualizer-en.html)**

A browser-based, step-by-step Java execution visualizer inspired by [MOOC.fi](https://www.mooc.fi/en/) and [PythonTutor](https://pythontutor.com/).  
No installation needed — just open the link above or download the HTML file.

### What It Does

Helps beginners understand two of Java's most confusing concepts:

- **Compile-Time Overload Resolution** — How the compiler picks a method based on *static type*
- **Runtime Dynamic Dispatch** — How the JVM finds the actual method body at runtime based on *dynamic type*

### Features

| Feature | Description |
|---|---|
| ✏️ Write any Java code | Type your own classes, inheritance chains, method calls |
| ▶ Step-by-step execution | Navigate with **Prev / Next** buttons or `←` `→` arrow keys |
| 🔵 Blue `►` highlight | Current call site line |
| 🟢 Green `⤷` highlight | Method body that execution **jumped into** |
| ⚙ Compile-Time analysis | Candidates, selected signature, widening (`int→double`) |
| ⚡ Runtime analysis | Class hierarchy, override detection, actual method executed |
| 🧠 Memory panel | Live Stack (variables) + Heap (objects) at every step |
| 💬 Explanation box | Plain-language description of what is happening at each step |
| 🖥 Output panel | Console output accumulates line by line |

### Built-in Examples

- **Ober / Unter** — Classic overloading + widening + dynamic binding
- **Animal / Dog / GoldenRetriever** — 3-level inheritance with overriding
- **Shape / Circle / ColoredCircle** — Multiple overloads + multi-level override

### Concepts Demonstrated

```java
Ober o = new Unter();   // Static type: Ober | Dynamic type: Unter
o.print(5);             // CT: Ober.print(double) selected (int→double widening)
                        // RT: Unter.print(double) executed (override)
```

### Technical Details

- No dependencies — Pure HTML + CSS + vanilla JavaScript
- No build step — single file, works offline
- Parser: regex-based Java subset parser
- Type system: full primitive widening chain (`byte→short→int→long→float→double`)
- Overload resolution: most-specific method selection with widening cost sorting
- Dynamic dispatch: virtual method table simulation via class hierarchy walk

### License

MIT — free to use, modify, and share.

---

## 🇹🇷 Türkçe

### 🔗 Canlı Demo
> **[▶ Java Step Visualizer'ı Aç (Türkçe)](https://canerztk8.github.io/java-step-visualizer/java-visualizer-tr.html)**

MOOC.fi ve PythonTutor'dan ilham alınan, tarayıcıda çalışan adım adım Java yürütme görselleştiricisi.  
Kurulum gerekmez — yukarıdaki linke tıkla veya HTML dosyasını indir.

### Ne Yapar?

Java'nın en kafa karıştırıcı iki konusunu yeni başlayanlar için görselleştirir:

- **Compile-Time Overload Resolution** — Derleyicinin *statik tipe* bakarak metodu nasıl seçtiği
- **Runtime Dynamic Dispatch** — JVM'in çalışma zamanında *dinamik tipe* bakarak gerçek metot gövdesini nasıl bulduğu

### Özellikler

| Özellik | Açıklama |
|---|---|
| ✏️ İstediğin Java kodunu yaz | Kendi sınıflarını, kalıtım zincirini, metot çağrılarını yaz |
| ▶ Adım adım yürütme | **Prev / Next** butonları veya `←` `→` ok tuşlarıyla ilerle |
| 🔵 Mavi `►` vurgu | O anda çağrının yapıldığı satır |
| 🟢 Yeşil `⤷` vurgu | Yürütmenin **atladığı** metot gövdesi satırı |
| ⚙ Compile-Time analizi | Adaylar, seçilen imza, widening (`int→double`) |
| ⚡ Runtime analizi | Sınıf hiyerarşisi, override tespiti, çalışan gerçek metot |
| 🧠 Bellek paneli | Her adımda canlı Stack (değişkenler) + Heap (nesneler) |
| 💬 Açıklama kutusu | Her adımda ne olduğunu anlatan sade Türkçe metin |
| 🖥 Output paneli | Konsol çıktıları satır satır birikerek eklenir |

### Dahili Örnekler

- **Ober / Unter** — Klasik overloading + widening + dynamic binding örneği
- **Animal / Dog / GoldenRetriever** — 3 seviyeli kalıtım ve override
- **Shape / Circle / ColoredCircle** — Çoklu overload + çok seviyeli override

### Gösterilen Kavramlar

```java
Ober o = new Unter();   // Statik tip: Ober | Dinamik tip: Unter
o.print(5);             // CT: Ober.print(double) seçildi (int→double widening)
                        // RT: Unter.print(double) çalıştırıldı (override)
```

### Teknik Detaylar

- Bağımlılık yok — Saf HTML + CSS + vanilla JavaScript
- Build adımı yok — tek dosya, internetsiz çalışır
- Parser: regex tabanlı Java alt kümesi ayrıştırıcı
- Tip sistemi: tam ilkel genişleme zinciri (`byte→short→int→long→float→double`)
- Overload çözümü: widening maliyeti sıralamasıyla en spesifik metot seçimi
- Dynamic dispatch: sınıf hiyerarşisinde sanal metot tablosu simülasyonu

### Lisans

MIT — kullan, değiştir, paylaş.
