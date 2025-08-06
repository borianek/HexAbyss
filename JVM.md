<!-- JVM.md -->

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
