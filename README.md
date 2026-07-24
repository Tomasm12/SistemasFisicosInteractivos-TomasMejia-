# SistemasF-sicosInteractivos-TomasMejia-

##Investigacion 
Codigo 



```Java
setcpm(24)

let armonia = chord("Fmaj7@4 C@4 G@4 Am7@4").voicing().sound("gm_epiano1").room(0.3).v(0.65);
$armonia: armonia

let melodia = note("[c5 e5 g5 e5] [a4 c5 f5 c5] [b4 d5 g5 d5] [c5 e5 a5 e5]")
  .sound("piano")
  .v(1.1);
$melodia: melodia


let bajo = note("[f2 ~ f2 ~]@1 [c2 ~ c2 ~]@1 [g2 ~ g2 ~]@1 [a2 ~ a2 ~]@1")
  .sound("triangle")
  .v(0.7);
$bajo: bajo


let cuerdas = note("a4@2 ~@2 g4@2 ~@2 b4@2 ~@2 c5@2 ~@2")
  .sound("gm_violin")
  .attack(0.2)
  .legato(0.5)
  .room(0.2)
  .v(0.45);
$cuerdas: cuerdas


let arpeggio = note("f4 c5 e5 c5 c5 g5 b5 g5 g4 d5 b5 d5 a4 e5 c5 e5")
  .sound("gm_epiano2")
  .room(0.2)
  .v(0.3);
$arpeggio: arpeggio


let textura = note("c6 ~ ~ g6 ~ e6 ~ ~")
  .sound("piano")
  .room(0.2)
  .v(0.35);
$textura: textura

let ritmo = stack(
  s("bd").beat("0,8,10", 16),
  s("hh").beat("0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15", 16).v("0.4 0.2"),
  s("sd").beat("4,12", 16).v(0.35),
  s("rim").beat("14", 16).v(0.3)
).lpf(slider(3254, 500, 5000)).v(0.55);
$ritmo: ritmo
```

[SFI Tomas]([file:///C:/Users/USUARIO/Documents/UPB/S8/Investigacion%20SFI%20%20TM.html](https://strudel.cc/#Ly8gUHJlYmFrZSBzY3JpcHQKLy8KLy8gVGhpcyBpcyBjb2RlIHRoYXQgaXMgbG9hZGVkIGJlZm9yZSB5b3VyIHBhdHRlcm4gaXMgcnVuLgovLyBZb3UgY2FuIHVzZSBpdCB0byBkZWZpbmUgY3VzdG9tIGZ1bmN0aW9ucyB0byB1c2UgaW4gYW55IHBhdHRlcm4uCi8vIAovLyBUaGlzIGlzIGFuIGluaXRpYWwgZXhhbXBsZSBzY3JpcHQuIFlvdSBjYW4gZWRpdCBpdCB0byBhZGQgCi8vIHlvdXIgb3duIGZ1bnRpb25zLgovLwovLyBUbyB1c2UgYSBzY3JpcHQgc2hhcmVkIGJ5IHNvbWUgb3RoZXIgdXNlciB5b3UgY2FuIHVzZQovLyB0aGUgaW1wb3J0LWJ1dHRvbiBvciBwYXN0ZSB0aGUgc2NyaXB0IGluIHRoaXMgZWRpdG9yLgoKY29uc3QgcmF0Y2hldCA9IHJlZ2lzdGVyKCdyYXRjaGV0JywgKHBhdCkgPT4gcGF0LnNvbWV0aW1lcyhwbHkoMikpKQoKc2V0Y3BtKDI0KQoKbGV0IGFybW9uaWEgPSBjaG9yZCgiRm1hajdANCBDQDQgR0A0IEFtN0A0Iikudm9pY2luZygpLnNvdW5kKCJnbV9lcGlhbm8xIikucm9vbSgwLjMpLnYoMC42NSk7CiRhcm1vbmlhOiBhcm1vbmlhCgpsZXQgbWVsb2RpYSA9IG5vdGUoIltjNSBlNSBnNSBlNV0gW2E0IGM1IGY1IGM1XSBbYjQgZDUgZzUgZDVdIFtjNSBlNSBhNSBlNV0iKQogIC5zb3VuZCgicGlhbm8iKQogIC52KDEuMSk7CiRtZWxvZGlhOiBtZWxvZGlhCgoKbGV0IGJham8gPSBub3RlKCJbZjIgfiBmMiB%2BXUAxIFtjMiB%2BIGMyIH5dQDEgW2cyIH4gZzIgfl1AMSBbYTIgfiBhMiB%2BXUAxIikKICAuc291bmQoInRyaWFuZ2xlIikKICAudigwLjcpOwokYmFqbzogYmFqbwoKCmxldCBjdWVyZGFzID0gbm90ZSgiYTRAMiB%2BQDIgZzRAMiB%2BQDIgYjRAMiB%2BQDIgYzVAMiB%2BQDIiKQogIC5zb3VuZCgiZ21fdmlvbGluIikKICAuYXR0YWNrKDAuMikKICAubGVnYXRvKDAuNSkKICAucm9vbSgwLjIpCiAgLnYoMC40NSk7CiRjdWVyZGFzOiBjdWVyZGFzCgoKbGV0IGFycGVnZ2lvID0gbm90ZSgiZjQgYzUgZTUgYzUgYzUgZzUgYjUgZzUgZzQgZDUgYjUgZDUgYTQgZTUgYzUgZTUiKQogIC5zb3VuZCgiZ21fZXBpYW5vMiIpCiAgLnJvb20oMC4yKQogIC52KDAuMyk7CiRhcnBlZ2dpbzogYXJwZWdnaW8KCgpsZXQgdGV4dHVyYSA9IG5vdGUoImM2IH4gfiBnNiB%2BIGU2IH4gfiIpCiAgLnNvdW5kKCJwaWFubyIpCiAgLnJvb20oMC4yKQogIC52KDAuMzUpOwokdGV4dHVyYTogdGV4dHVyYQoKbGV0IHJpdG1vID0gc3RhY2soCiAgcygiYmQiKS5iZWF0KCIwLDgsMTAiLCAxNiksCiAgcygiaGgiKS5iZWF0KCIwLDEsMiwzLDQsNSw2LDcsOCw5LDEwLDExLDEyLDEzLDE0LDE1IiwgMTYpLnYoIjAuNCAwLjIiKSwKICBzKCJzZCIpLmJlYXQoIjQsMTIiLCAxNikudigwLjM1KSwKICBzKCJyaW0iKS5iZWF0KCIxNCIsIDE2KS52KDAuMykKKS5scGYoc2xpZGVyKDMyNTQsIDUwMCwgNTAwMCkpLnYoMC41NSk7CiRyaXRtbzogcml0bW8%3D))
