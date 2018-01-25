# vef2018verk1

### 1.Hvað er Ubuntu Server? Útskýrðu með eigin orðum (50 orð). (0.5%)
---------
Ubuntu er stýrikerfi í Linux fjölskyldunni sem er byggt á Debian arkitektúr.
Það er bæði notað á persónulegar tölvur og vefþjónar en mér þinnst það vera meiri merkilegt sem vefþjónn.
Það er vinsælasti stýrikerfið fyrir "cloud computing" og er líka vinsælasti linux kerfið fyrir vefþjóna.
Eins og margir aðrir linux kerfi það er open source sem þýðir allir geta fengið uppsprettu kóðann fyrir aftan kerfið.
### 2.Apache eða Nginx vefþjónn (http server)? Hvað gera þeir? Hver er munurinn á þeim? (lágmark 50 orð). (0.5%)
---------
Apache og Nginx eru bæðu með margt sameiginlegt og eru notuð víða á netinnu að þjóna yfir 50% af umferðinni saman.
###### Apache
Robert McCool gerði Apache í 1995, og varð þróuð af Apache Software Foundation síðan 1999
Apache er mest vinsælasti vefþjónnin síðan 1996 enn hefur verið að missa vinsældin til Nginx og Microsoft ISS nýlega, enn það hefur samt mikla skjalfestinga og inbyggðan stuðning frá önnur forrit vegna vinsældinni.
Apache er oft valin fyrir sveiganleika, mátt og víðan stuðning.

###### Nginx
Árið 2002 Igor Sysoev hannaði Nginx sérstaklega fyrir frammistöðu takmarkanir sem Apache vefþjónarnir hafði sem lausn til að taka við meiri umferð og er að fá meiri notkun fyrir að setja lítinn álag á tölvur og að geta stækkið þjónustu hæfileika á lágmarks vélbúnaði.
Það er hannað til að þjóna static síður og gefa dynamic skipanir til önnur forrit.
Nginx er oft valin fyrir lágmarks álag á vélbúnað og móttæk undir miklan umferð.

Það er mikill samkeppni á milli forritin á flest svæði en Nginx er betri með static og bæði forrit eru sambærileg annarsvegar.

Notendur sem nota "Shared hosting" munu finna meira hentugt að nota Apache .htaccess og auka stuðninging fyrir Apache frá önnur forrit.

### 3.Eftirfarandi application servers (ásamt fleirum) er hægt að nota fyrir python á server. Berðu þá saman (kosti og galla) og útskýrðu nánar tilgang þeirra. (lágmark 100 orð). (1%)
###### a. Common Gateway Interface (CGI)
Það býður upp á samskiptareglur fyrir vef þjóna til að keyra forrit sem keyra eins og command-line interface forrit sem keyra á vef þjón sem myndar dynamic HTML vefsíður. Common Gateway Interface eru líka kölluð CGI scripts eða bara CGI.
###### b. mod_python
Það er Apache HTTP server forrit sem samæettir python með vefþjónin, það var meira skilvirkt miðað CGI vegna þess CGI þarfnast nýtt python ferli í hvert sinn fyrir hverja einustu vef skipanir.
Áhugin á mod_python hefur fært yfir til mod_wsgi eftir python þróaði "Web Server Gateway Interface" og að lokum engin er að vinna á mod_python.
###### c. FastCgi and SCGI
FastCgi er útgáfa af CGI sem er hraðari og var þróuð með markmiðinna til að létta hægðir á háum net og til að vera samkeppnishæf við önnur forrit sem eru enn notuð í dag.
SCGI er önnur útgáfa af CGI sem er lík FastCgi enn er hönnuð til að vera léttara að framkvæma og leifir CGI forrit með mikla seinkun til að virka.
###### d. mod_wsgi
Mod_wsgi er önnur Apache HTTP server forrit og styður við python 2.6 og python 3.2, það er annað val á móti mod_python, CGI og FastCgi.
###### e. Gunicorn
Gunicorn er Python WSGI HTTP þjón tekin frá Ruby's unicorn verkefnið og er samhæft við marga vef ramma eins og django.
###### f. uWSGI
Forrit fyrir hýsinga þjónustur, cherokee og NGINX þjónar eru bútaðir til að vinna með uWSGI best.

### 4.Útskýrðu ferlið og tengsl milli Ubuntu, vefþjóni og application server útfrá request/respone frá biðlara (client) (lágmark 50 orð og skýringamynd) (0.5%)
Ubuntu er Stýrikerfið og er vinsælasti stýrikerfið í Linux fjölskyldunni fyrir vefþjóna, vefþjónnin er geymd einhverstaðar sem vonandi hefur netsamband og application hefur forritin eins og python og html. 
Stýrikerfið setur allt í gang eins og vefþjónin og stjórnar auðlindirnar sem hvert forrit fær að nota, vefþjónnin kemur skilaboðinn/vefsíðum til skila og application hefur forritin.
https://qph.ec.quoracdn.net/main-qimg-1718f67b27fbda7119d7bac5ccef91df
### 5.Hvað er pip og tilgangur þess? (0.5%)
PIP tekur við, packar og flytur hugbúnað inn eða út.
pip standur fyrir Pip installs packages eða Pip installs python
### 6.Hver er helsti munurinn á http 1.1 og http 2.0 (0.5%)
Þetta er mjög víð spurning en munin á 1.1 og 2.0 geta verið þýdd að 2.0 er miklu hraðari.

### 7.Hvað er SSH og SSH key. Hvenær er heppilegt að nota SSH key? (0.5%)
Secure Shell(SSH) er dulrituð net samskiptareglur fyrir að keyra net þjónustur yfir netið örugglega.

SSH lyklal þjóna sem leið til að auðkenna þig í SSH vefþjónn.
### 8.Hvað er ,,two-factor authentication" Komdu með dæmi og kosti og galla. (0.5%)
two-factor authentication (2FA), er öryggisaðferð þar sem notandin verður að sýna sönnun(factors) til auðkenninga búnaðin sem er eitt eða meira af: þekkingu sem bara þeir vita(PIN númer), eign á sérstakan hlut(eins og disconnected eða connected token generator eða síminn þinn), eða sönnun að þetta eru þeir(fingrafara skanni, augn skanni, radd skynjari)
kostir:
þekkinging eru auka lykilorð
þú hefur síman/lykla

gallar:
aðrir geta líka munið eða stolið PIN númerin og lykilorð.
Þú þart að hafa token generator eða síma með generator app með þér allan tímann og með connected token þú gæti þurft að stinga inn USB á hvert skipti og annarsvegar þurfa skrifa tokenið.
Augn skannar og fingrafara skannar eru ekki algengir.
### 9.Hvað er IPv6, skiptir það einhverju máli? kostir og gallar. (0.5%)
---------

### 10.Settu upp flask á Ubuntu 16.04 á Digital Ocean. Skrifaðu nafnið þitt með python, html og css í rauðum lit. (5%)
---------

#### Auka:
Notaði þennan lausn til að komast á skóla emailið

https://answers.microsoft.com/en-us/outlook_com/forum/oaccount-omyinfo/cant-access-microsoft-outlook-email-because-of/37122618-d538-4d7d-ae2d-4f883d24bb4d?auth=1

hafðu það geymt einhverstaðar svo þú *getur* reynt að hjálpa næsta nemandan sem hefur sama vandamálið
