## 🌐 Wybór Języka

Proszę wybrać preferowany język poniżej:


<details>
  <summary>🔹 <strong>🇵🇱 Polski</strong></summary>
  
<h1 align="center">
🚀 Konfiguracja Argumentów JVM dla<br>
Hex:Abyss 𝕃𝕀𝕋𝔼 Modpack
</h1>

<p align="center"><strong>O co chodzi?</strong><br>
Ten plik zawiera rekomendowane argumenty <code>JVM</code>, które należy dodać do launchera  
(<em>CurseForge</em>, oficjalny Minecraft launcher lub <em>TLauncher</em>)  
do uruchomienia <a href="https://github.com/borianek/HexAbyss?tab=readme-ov-file#-modpack--odmiany-" target="_blank"><strong>LITE</strong></a> odmiany modpacka <span style="color:#FF6B6B;"><strong>Hex:Abyss</strong></span>.
</p>

---

## 🎯 Argumenty JVM

Zamieść poniższy blok w polu **JVM Arguments** lub **Additional Arguments** swojego launchera:

```yaml
-Xms3G
-Xmx4G
-XX:+UseG1GC
-XX:+UnlockExperimentalVMOptions
-XX:G1NewSizePercent=20
-XX:G1MaxNewSizePercent=40
-XX:G1HeapRegionSize=8M
-XX:G1ReservePercent=20
-XX:MaxGCPauseMillis=50
-XX:G1MixedGCL
```

<h3 align="center" style="color:#4C9AFF;">🚀 Jak dodać te argumenty</h3>

<table>
  <thead>
    <tr>
      <th align="left">Launcher</th>
      <th align="left">Kroki</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>🔹 <strong>CurseForge</strong></td>
      <td>Wejdź w instancję modpacka → <strong>Ustawienia</strong> → pole <strong>Additional Arguments</strong></td>
    </tr>
    <tr>
      <td>🔹 <strong>Oficjalny launcher Minecraft</strong></td>
      <td><strong>Instalacje</strong> → Edytuj odpowiednią instancję → rozwiń <strong>Więcej opcji</strong> → pole <strong>JVM Arguments</strong></td>
    </tr>
    <tr>
      <td>🔹 <strong>TLauncher</strong></td>
      <td>Kliknij ikonę koła zębatego (Settings) → zakładka <strong>JVM arguments</strong></td>
    </tr>
  </tbody>
</table>

<div style="background-color:#F8D7DA; border-left:5px solid #F5C6CB; padding:10px; margin-top:1em;">
  <strong style="color:#721C24;">⚠️ Uwaga:</strong>  
  Te argumenty JVM oraz wersja <strong>LITE</strong> są przeznaczone wyłącznie dla użytkowników posiadających około <strong>8 GB RAM</strong>.
</div>

<h3 align="center">🚀 Co one robią? 🚀</h2>

<table>
  <thead>
    <tr>
      <th align="left">Argument</th>
      <th align="left">Opis</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>-Xms3G</code></td>
      <td>Ustala początkowy rozmiar sterty JVM na 3 GB, co gwarantuje przewidywalne zarządzanie pamięcią od samego startu.</td>
    </tr>
    <tr>
      <td><code>-Xmx4G</code></td>
      <td>Ogranicza maksymalny rozmiar sterty do 4 GB, chroniąc przed <em>OutOfMemoryError</em> i pozostawiając zasoby dla systemu operacyjnego.</td>
    </tr>
    <tr>
      <td><code>-XX:+UseG1GC</code></td>
      <td>Aktywuje Garbage-First Collector (G1GC), zoptymalizowany pod kątem aplikacji z dużymi obszarami sterty, jak Minecraft.</td>
    </tr>
    <tr>
      <td><code>-XX:+UnlockExperimentalVMOptions</code></td>
      <td>Odblokowuje zaawansowane, eksperymentalne opcje JVM niezbędne do pełnej konfiguracji G1GC.</td>
    </tr>
    <tr>
      <td><code>-XX:G1NewSizePercent=20</code></td>
      <td>Ustala minimalny rozmiar generacji młodej (Young Gen) na 20 % całkowitej sterty, zapewniając efektywne i częstsze krótkie cykle GC.</td>
    </tr>
    <tr>
      <td><code>-XX:G1MaxNewSizePercent=40</code></td>
      <td>Definiuje maksymalny udział Young Gen w stercie na 40 %, balansując czas i częstotliwość cykli odpadów.</td>
    </tr>
    <tr>
      <td><code>-XX:G1HeapRegionSize=8M</code></td>
      <td>Określa wielkość regionu sterty na 8 MB, umożliwiając bardziej granularne zarządzanie pamięcią i segregację obiektów.</td>
    </tr>
    <tr>
      <td><code>-XX:G1ReservePercent=20</code></td>
      <td>Rezerwuje 20 % sterty jako bufor dla procesów GC, zapobiegając nieoczekiwanemu rozszerzaniu pamięci.</td>
    </tr>
    <tr>
      <td><code>-XX:MaxGCPauseMillis=50</code></td>
      <td>Ustawia docelowy czas pauzy GC na maksymalnie 50 ms, co przekłada się na płynniejsze działanie gry.</td>
    </tr>
    <tr>
      <td><code>-XX:G1MixedGCLiveThresholdPercent=35</code></td>
      <td>Próg 35 % żywych obiektów w regionie decyduje o włączeniu go do mieszanego cyklu GC, optymalizując jego zakres.</td>
    </tr>
    <tr>
      <td><code>-XX:+AlwaysPreTouch</code></td>
      <td>Wymusza wstępne przydzielenie i „dotknięcie” całej sterty przy starcie JVM, minimalizując późniejsze opóźnienia GC.</td>
    </tr>
  </tbody>
</table>

<h4 align="center">🚀 A można prościej? 🚀</h4>
<div align="center">
  <table>
    <thead>
      <tr>
        <th align="left">Argument</th>
        <th align="left">Cel</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code>-Xms3G</code></td>
        <td>Początkowy RAM: 3 GB</td>
      </tr>
      <tr>
        <td><code>-Xmx4G</code></td>
        <td>Maksymalny RAM: 4 GB</td>
      </tr>
      <tr>
        <td><code>-XX:+UseG1GC</code></td>
        <td>Usprawnione sprzątanie pamięci</td>
      </tr>
      <tr>
        <td><code>-XX:+UnlockExperimentalVMOptions</code></td>
        <td>Odblokowanie opcji JVM</td>
      </tr>
      <tr>
        <td><code>-XX:G1NewSizePercent=20</code></td>
        <td>Min. 20 % dla nowych obiektów</td>
      </tr>
      <tr>
        <td><code>-XX:G1MaxNewSizePercent=40</code></td>
        <td>Max. 40 % dla nowych obiektów</td>
      </tr>
      <tr>
        <td><code>-XX:G1HeapRegionSize=8M</code></td>
        <td>Regiony sterty: 8 MB</td>
      </tr>
      <tr>
        <td><code>-XX:G1ReservePercent=20</code></td>
        <td>20 % RAM w rezerwie</td>
      </tr>
      <tr>
        <td><code>-XX:MaxGCPauseMillis=50</code></td>
        <td>Pauzy sprzątania < 50 ms</td>
      </tr>
      <tr>
        <td><code>-XX:G1MixedGCLiveThresholdPercent=35</code></td>
        <td>Sprzątanie przy ≥ 35 % użycia</td>
      </tr>
      <tr>
        <td><code>-XX:+AlwaysPreTouch</code></td>
        <td>Przygotowanie pamięci na start</td>
      </tr>
    </tbody>
  </table>
</div>


</details>

<details>
  <summary>🔹 <strong>🇬🇧 English</strong></summary>
  <h1 align="center">
🚀 JVM Arguments Configuration for<br>
Hex:Abyss 𝕃𝕀𝕋𝔼 Modpack
</h1>

<p align="center"><strong>What's this about?</strong><br>
This file contains the recommended <code>JVM</code> arguments to add to your launcher  
(<em>CurseForge</em>, the official Minecraft launcher, or <em>TLauncher</em>)  
to run the <a href="https://github.com/borianek/HexAbyss?tab=readme-ov-file#-modpack--variants-" target="_blank"><strong>LITE</strong></a> variant of the <span style="color:#FF6B6B;"><strong>Hex:Abyss</strong></span> modpack.
</p>

---

## 🎯 JVM Arguments

Place the following block in the **JVM Arguments** or **Additional Arguments** field of your launcher:

```yaml
-Xms3G
-Xmx4G
-XX:+UseG1GC
-XX:+UnlockExperimentalVMOptions
-XX:G1NewSizePercent=20
-XX:G1MaxNewSizePercent=40
-XX:G1HeapRegionSize=8M
-XX:G1ReservePercent=20
-XX:MaxGCPauseMillis=50
-XX:G1MixedGCL
```
<table>
  <thead>
    <tr>
      <th align="left">Launcher</th>
      <th align="left">Steps</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>🔹 <strong>CurseForge</strong></td>
      <td>Open the modpack instance → <strong>Settings</strong> → <strong>Additional Arguments</strong> field</td>
    </tr>
    <tr>
      <td>🔹 <strong>Official Minecraft Launcher</strong></td>
      <td><strong>Installations</strong> → Edit the desired profile → expand <strong>More Options</strong> → <strong>JVM Arguments</strong> field</td>
    </tr>
    <tr>
      <td>🔹 <strong>TLauncher</strong></td>
      <td>Click the gear icon (Settings) → <strong>JVM arguments</strong> tab</td>
    </tr>
  </tbody>
</table>
<div style="background-color:#F8D7DA; border-left:5px solid #F5C6CB; padding:10px; margin-top:1em;">
  <strong style="color:#721C24;">⚠️ Note:</strong>  
  These JVM arguments and the <strong>LITE</strong> version are intended only for users with around <strong>8 GB RAM</strong>.
</div>

<h3 align="center">🚀 What do they do? 🚀</h3>

<table>
  <thead>
    <tr>
      <th align="left">Argument</th>
      <th align="left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>-Xms3G</code></td>
      <td>Sets the JVM heap’s initial size to 3 GB, ensuring predictable memory management from the start.</td>
    </tr>
    <tr>
      <td><code>-Xmx4G</code></td>
      <td>Limits the maximum heap size to 4 GB, preventing <em>OutOfMemoryError</em> and leaving resources for the OS.</td>
    </tr>
    <tr>
      <td><code>-XX:+UseG1GC</code></td>
      <td>Enables the Garbage-First Collector (G1GC), optimized for applications with large heaps like Minecraft.</td>
    </tr>
    <tr>
      <td><code>-XX:+UnlockExperimentalVMOptions</code></td>
      <td>Unlocks advanced experimental JVM options required for full G1GC tuning.</td>
    </tr>
    <tr>
      <td><code>-XX:G1NewSizePercent=20</code></td>
      <td>Sets the young generation size to at least 20 % of the heap, yielding efficient, frequent short GC cycles.</td>
    </tr>
    <tr>
      <td><code>-XX:G1MaxNewSizePercent=40</code></td>
      <td>Limits the young generation to at most 40 % of the heap, balancing pause time and frequency.</td>
    </tr>
    <tr>
      <td><code>-XX:G1HeapRegionSize=8M</code></td>
      <td>Defines each heap region as 8 MB, allowing finer-grained memory management and object segregation.</td>
    </tr>
    <tr>
      <td><code>-XX:G1ReservePercent=20</code></td>
      <td>Reserves 20 % of the heap as a buffer for GC processes, preventing unexpected heap expansion.</td>
    </tr>
    <tr>
      <td><code>-XX:MaxGCPauseMillis=50</code></td>
      <td>Targets a maximum GC pause time of 50 ms, resulting in smoother gameplay.</td>
    </tr>
    <tr>
      <td><code>-XX:G1MixedGCLiveThresholdPercent=35</code></td>
      <td>Includes regions with ≥ 35 % live objects in mixed GC cycles, optimizing collection scope.</td>
    </tr>
    <tr>
      <td><code>-XX:+AlwaysPreTouch</code></td>
      <td>Forces the JVM to pre-touch the entire heap at startup, minimizing later GC latency spikes.</td>
    </tr>
  </tbody>
</table>

<h4 align="center">🚀 Is there, like, an easier way? 🚀</h4>
<div align="center">
  <table>
    <thead>
      <tr>
        <th align="left">Argument</th>
        <th align="left">Purpose</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code>-Xms3G</code></td>
        <td>Initial RAM: 3 GB</td>
      </tr>
      <tr>
        <td><code>-Xmx4G</code></td>
        <td>Max RAM: 4 GB</td>
      </tr>
      <tr>
        <td><code>-XX:+UseG1GC</code></td>
        <td>Improved memory cleanup</td>
      </tr>
      <tr>
        <td><code>-XX:+UnlockExperimentalVMOptions</code></td>
        <td>Unlock JVM options</td>
      </tr>
      <tr>
        <td><code>-XX:G1NewSizePercent=20</code></td>
        <td>Min. 20 % for new objects</td>
      </tr>
      <tr>
        <td><code>-XX:G1MaxNewSizePercent=40</code></td>
        <td>Max. 40 % for new objects</td>
      </tr>
      <tr>
        <td><code>-XX:G1HeapRegionSize=8M</code></td>
        <td>Heap regions: 8 MB</td>
      </tr>
      <tr>
        <td><code>-XX:G1ReservePercent=20</code></td>
        <td>20 % RAM reserved</td>
      </tr>
      <tr>
        <td><code>-XX:MaxGCPauseMillis=50</code></td>
        <td>GC pauses &lt; 50 ms</td>
      </tr>
      <tr>
        <td><code>-XX:G1MixedGCLiveThresholdPercent=35</code></td>
        <td>Trigger GC ≥ 35 % live usage</td>
      </tr>
      <tr>
        <td><code>-XX:+AlwaysPreTouch</code></td>
        <td>Pre-touch memory on startup</td>
      </tr>
    </tbody>
  </table>
</div>


</details>
