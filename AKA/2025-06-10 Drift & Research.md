
![[{293B6314-7F1E-4965-89DD-D3C08E6332A4}.png]]

VDI01 køre er låst.
1. Det ser ud til at det er Tjek og server som er stuck på "Get Data Manager"
	1. Dette er sket før
	2. Kunne være DWH forbindelse som skaber problemer eftersom at en opdatering hertil kom, og fejlen er først begyndt herefter.
		1. Kunne også godt være en anden årsag, da både VDI01 og 02 Begynder er give nye fejl.
2. Løst ved at 'Kill' T&S Proces.
	1. Alt kørte fint herefter

Fejl på F34:
- Modulus Fravær Billede kan ikke loade data i hele CRM
	- Systemfejl fra STAR

Fejl på NUPH
- Ny selector - CRM har ukente "mellemrum" i titlen.
	- Dette er muligt kommet efter en update.


Research todo:
1. DWH Connection
	1. Muligt Conn
2. Framework Kill-safe
	1. Hvis en robot