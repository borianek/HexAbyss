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
