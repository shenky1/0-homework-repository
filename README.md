# 0-homework-repository
C# FER 0th homework repository

# JMBAG
1191230022

#Pitanje 1:
Nakon što sam dodao class library kao referencu u projekt konzolna aplikacija, debug direktorij konzolne aplikacije se promijenio. Dodani su .dll i .pdb datoteke od ClassLibrary projekta. Kada sam obrisao classLibrary.dll iz istog direktorija i pokrenuo aplikaciju konzolnaAplikacija.exe dobio sam FileNotFoundException'. To se dogodilo jer konzolnaAplikacija ovisi o MyConsole.PrintHelloWorld metodi cija se implementacija nalazi u classLibrary.dll datoteci. Kada bih slao aplikaciju, poslao bih kompletan sadrzaj bin/Debug foldera, onako kako je buildom izgenerirano.

#Pitanje 2:
Kada stisnem start ikonu u VS automatski se builda (kompajlira) čitav projekt i oni ovisni projekti ako postoje. Ako samo promijenim i saveam MyConsole.PrintHelloWorld() metodu i pokrenem KonzolnaAplikacija.exe u debug folderu ništa se ne dogodi jer se build i compile nije izvršio koji update-a dll datoteku te međukod.

#Pitanje 3:
Pero: Hello World

#Pitanje 4:
Dodan je PeroClassLibrary.dll, ali ne i .pdb.

#Pitanje 5:
Aplikacija i dalje radi jer se nakon prvog builda .dll datoteka kopirala u debug direktorij projekta u kojem je korištena. Ovisnost o originalnoj .dll datoteci prebacila se na tu kopiranu .dll datoteku. Sada se u VS datoteka traži u folderu u kojem je projekt path = ...\visual studio 2015\Projects\NultaDZ\KonzolnaAplikacija\bin\Debug\PeroClassLibrary.dll

#Pitanje 6:
Buildanje projekta ponovno je stvorio packages direktorij. To je zato jer je u konzolnoj aplikaciji ostala packages.config. Nakon što sam i to pobrisao ništa se nije dogodilo. 

