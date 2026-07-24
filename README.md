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

[SFI Tomas](file:///C:/Users/USUARIO/Documents/UPB/S8/Investigacion%20SFI%20%20TM.html)
