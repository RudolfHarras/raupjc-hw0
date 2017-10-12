# Pitanje 1 :
Osim dosadasnjih fileova, u folderu je dll s imenom class library projekta
Dogodi se iznimka, i to sljedeca: System.IO.FileNotFoundException: Could not load file or assembly 'ClassLibrary1, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null' or one of its dependencies. The system cannot find the file specified.    
 at ConsoleApplication.Program.Main(String[] args)
To se dogodi jer exe trazi MyConsole.PrintHelloWorld, ali kako je dll obrisan, ne moze ga naci, a sam MyConsole nije po defaultu u GAC-u te dolazi do naredbe za koju ne zna znacenje.
Treba se poslati exe file, ali i dll ClassLibrary1 (ime naravno moze varirati)

 
# Pitanje 2 :
Konzolna aplikacija je iskoristila staru verziju. Ona koristi onu verziju koju moze koristiti, a kako library nije preveden, koristi proslu verziju.

# Pitanje 3 :
Build proces je uspio, ali je javio "Restoring NuGet packages..." prije toga.
packages direktorij opet ima u sebi NodaTime folder koji je ponovno vraćen na mjesto nakon brisanja

