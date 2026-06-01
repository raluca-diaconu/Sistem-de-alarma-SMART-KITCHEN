# Sistem de alarma pentru o bucatarie inteligenta si moderna (smart kitchen). 
Siguranta omului este importanta, in special cand este nevoit sa gateasca pentru ca poate intampina mai multe pericole: foc, fum, scurgeri de gaze. Din acest motiv, fiecare bucatarie are nevoie de un sistem de alarma performant care sa fie capabil sa atraga atentia asupra pericolului si, astfel, sa ii ofere posibilitatea omului de a actiona in timp util. 

Sistemul pe care mi l-am imaginat are capacitatea de a detecta prezenta gazelor nocive sau a fumului si a flacarilor deschise. De asemenea, preia informatii despre calitatea aerului (nivelul de gaz) si temperatura camerei. Acesta e capabil si sa detecteze prezenta persoanelor si sa intre in modul de economisire a luminii in timpul zilei. Sistemul poate fi dezvoltat, de ex: atunci cand este detectata o persoana noaptea, lumina se aprinde.

Eu am facut varianta mai simpla a sistemului: alarma si mesaj cand sunt detectate foc si fum, mesaj cu informatii despre temperature si gaz, mesaj de bun venit la detectarea miscarii si aprinderea luminii de fundal pe intuneric. 

Lista de componente:

•	Placa de dezvoltare Arduino Uno R3 + cablu USB;

•	Modul senzor de gaz MQ-135 (analogic);

•	Modul senzor de temperatura DHT11 cu led (digital);

•	Senzor ultrasonic de distanta HC-SR04+ (digital);

•	Modul cu fotorezistor (senzor de lumina rezistiv) (analogic);

•	Modul senzor de flacara infrarosu (digital);

•	Modul LCD 1602 cu Backlight Galben-Verde + Adaptor I2C;

•	Breadboard HQ830 + fire;

•	Fire mama-tata;

•	Buzzer Activ cu sunet continuu SFM-27. 

Functionare:

	Senzorul de gaz: da informatii despre nivelul de gaz, iar arduino afiseaza pe ecran (ex: „G: 200”). Cand un prag este depasit (ex: 600), alarma de la buzzer este activata si un mesaj: „Alerta! Gaz detectat!” apare pe ecran. 

	Senzorul de foc: Cand este activat (adica simte foc in apropiere), alarma de la buzzer este activata si un mesaj: „Alerta! Foc detectat!” apare pe ecran.
Daca senzorul de foc e activat si pragul gazului este depasit, alarma de la buzzer este activata si un mesaj: „Alerta! Foc + gaz” apare pe ecran.

	Senzorul de lumina: este citita valoarea luminii. Daca aceasta depaseste un prag (ex: 40), lumina de fundal a ecranului se stinge (semn ca e zi – intra in modul de economisire a energiei). Daca nu depaseste pragul, lumina de fundal se aprinde (semn ca e noapte).

	Senzorul de distanta: se citeste timpul in care un sunet transmis de senzor se loveste de un obstacol si se intoarce la senzor. Timpul este prelucrat si transformat in distanta. Daca distanta este mai mica de un prag (ex: 40), pe ecran apare un mesaj: „Bun venit!” (adica e detectata prezenta unui om). 

	Senzorul de temperatura: transmite tensiunea pe care o primeste de la pin. Aceasta tensiune e transformata in temperatura Celsius. Aceasta temperatura este afisata pe ecran (ex: T: 440C).
