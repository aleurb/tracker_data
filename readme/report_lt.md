@title   : Stimuliacijos poveikis širdies ritmui
@data    : 2025-01-30
@autorius: Aleksandras Urbonas

1. Pagrindinis klausimas: ar stimuliacija turi įtakos širdies ritmo rodikliams?
	- Remiantis analize, nustatyta, kad vartotojai (N=2361), kurie dalyvavo „Programoje“ – nurodant stimuliaciją – (bent S=10 seansų) – vidutinis ŠSD pokytis –0,03 k./min (sumažėjimas).
	- Poveikis seansų metu skyrėsi, o didžiausias pastebėtas pokytis buvo 95,00 k./min.
	- Įžvalgos nustatytos pagal `Sessions` ir `Daily` duomenis.

2. Antrinės įžvalgos:
	- Papildomi veiksniai, darantys įtaką HR pokyčiams: seanso trukmė, paros laikas (reikalinga tolesnė analizė dėl sezoniškumo modelių).
	- Svarbi analizė pagal prietaiso tipą (toliau).
	- Daug laiko buvo skirta duomenų tyrinėjimui ir schemų supratimui. Išsamesnė schema ir verslo proceso aprašymas gali padėti.
	- `Samples` duomenyse yra ~70 mln. įrašų, todėl analizė suletėja. Rekomenduojama tokius duomenis apdoroti SQL, pvz., atliekant agregacijas pagal vartotoją skirtingu laikotarpiu. Šiame tyrime Samples buvo pradėtas tikrinti, bet po komandos patvirtinimo, paliktas tolimesnėm analizėms.
	- Atliktas duomenų validavimas: klaidingi/trūkstami duomenys pašalinami automatiškai.
	- Duomenys buvo analizuojami naudojant Python, todėl analizę galima pakartoti.