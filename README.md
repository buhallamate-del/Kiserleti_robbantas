# Kísérleti Lőtér

Egyfájlos böngészős játék – az `index.html` megnyitásával fut.

## Űrverseny (több játékos)

Heti futam más játékosok ellen (a Program lapon vagy a főmenüben: „Űrverseny”). Aki beszáll, új programot kezd
Főkonstruktőr nehézségen; a mostani játék félrekerül, kilépéskor pontosan ott folytatódik. A versenyjáték a héten
bármikor folytatható, hétfőn új futam indul.

- **Rangsor:** a mérföldkövek (szuborbitális ugrás, műhold, ember az űrben, holdszonda, űrállomás, Holdraszállás)
  száma; azonos számnál az nyer, aki kevesebb negyedév alatt érte el az utolsót. Így az is versenyezhet, aki nem
  egyszerre játszik a többiekkel.
- **Elsőség:** aki a héten valós időben elsőként ér el egy mérföldkövet, presztízst és pénzt kap (a második +10 presztízst).
- **Élő hírek:** a többiek indításai és mérföldkövei a naplóba és értesítésként érkeznek; látszik, ki van épp fent.
- **Technika:** nyilvános MQTT üzenetközvetítő (HiveMQ, WebSocket), mint a Raktár 3D-ben; saját szerver nincs.
  Csak a program neve és a versenyállás megy át. A könyvtár: `vendor/mqtt/` (MIT licenc).

## Három univerzum

A Kísérleti Lőtér az [Eseményhorizonttal](https://buhallamate-del.github.io/Esemenyhorizont/) és a [Raktár 3D-vel](https://buhallamate-del.github.io/raktar-3d/) közös naplót vezet (a böngésző tárhelyében, kulcs: `univerzum-naplo`). Ha egy terhet szökési sebességre gyorsítasz, a Program lapon megjelenik a „Furcsa jel a mélyűrből” kártya: a jelet követve az Eseményhorizontba jutsz, ahol a szondád a fekete lyuk körül kering. Ha ott megtalálod a Lőtér titkos buborékját, itt kutatási támogatás érkezik (+100 M, egyszer); ha a Raktár 3D-ben rátalálsz a fekete lyukra, az Akadémia is felfigyel (+20 presztízs, egyszer).
