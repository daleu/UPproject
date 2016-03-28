# BotiguesBCN - PLA DE DESENVOLUPAMENT DE SOFTWARE #

> El propòsit del document de pla de desenvolupament de software és determinar l'esforç, cost i calendari a nivell de projecte (distingint només les 4 fases)


## 1. ORGANITZACIÓ I EQUIP ##

> Descriure breument l'organització i l'equip de treball (quins rols, quants treballadors de cada rol)

El sistema BotiguesBCN ha de ser senzill, eficaç i agradable d’usar. El nostre projecte consisteix en el desenvolupament i manteniment de una aplicació mòvil i web, per tant, el nostre equip haurà de ser especialista en aquest àmbit.
El nostre equip de treball estara organitzat respecte la seva funció sobre el desenvolupament, manteniment i supervisió del sistema.
Distingirem entre els seguents rols de treball:

* Cap del projecte. Es la persona responsable de gestionar el projecte. Es necessita de molta experiència i coneixements en el camp dels projectes.
* Arquitecte (Cap Tècnic). Es la persona responsable de crear un entorn de treball on la gent es trobi a gust i autoritzada per fer qualsevol de les seves tasques o responsabilitats.
* Dissenyador. Es la persona encarregada de transformar els requisits del usuari en un disseny arquitectònic que proveira d'especificacions als programadors.
* Programador Semi-Senior. Programador amb experiència i especialista en diversos camps. Té capacitat de treball autonom i qualitat en programar.
* Analista Funcional. Es la persona responsable de supervisar el desenvolupament de la aplicació mòvil i web. Assegurant-se la màxima explotació del entorn i que disposi de un rediment òptim.
* Analista de Xarxes. Es la persona responsable de dissenyar i gestionar la seguretat de la Xarxa que usara l'aplicació.
* Administrador Base de Dades. Es la persona responsable dels aspectes d'entorn de la Base de Dades que utilitzara l'aplicació.
* Tester. Es la persona responsable de realitzar proves a l'aplicació i reporta els seus errors abans de la sortida d'aquesta al públic.

|Rol|Persones| 
|---|---|
|Cap del projecte|1|
|Arquitecte|1|
|Dissenyador|1|
|Programador Semi-Senior|4|
|Analista Funcional|1|
|Analista de Xarxes|1|
|Administrador Base de Dades|1|
|Tester|10|

## 2. PLA DE PROJECTE ##

### 2.1. Estimació d'esforç ###

> Calcular el nombre d'hores del projecte. Useu un excel o altra eina per calcular UCPs i convertir a hores. Copieu aquí les taules (però entregueu també l'excel!)

**ESTIMACIÓ TCF**

|Descripció|Pes|Prioritat|
|---|---|---|
|Sistema distribuït|1|5|
|Rendiment|2|3|
|Eficiencia del Usuari Final|2|5|
|Processamet intern complex|0.5|1|
|Reusabilitat|1|4|
|Fàcil de instalar|-1|5|
|Fàcil d'usar|0.5|5|
|Portabilitat|0.5|4|
|Fàcil de canviar|2|3|
|Característiques especials de seguretat|1|5|
|Accés directe desde tercers|1|5|
|Es necessiten usuaris experts o entrenats|-1|3|

**ESTIMACIÓ ECF**

|Factor d'Entorn|Pes|Avaluació|
|---|---|---|
|Capacitat analistica|0.5|3|
|Dificultat del llenguatge de programació|-1|2|
|Estabilitat dels requisits|2|3|
|Experiència en l'aplicació|0.5|3|
|Experiència en Orientació a Objectes|1|3|
|Familiarització amb l'UML|1.5|2|
|Motivació|1|2|
|Treball a temps parcial|-1|1|

**ESTIMACIÓ UAW**

|Actor|Pes|
|---|---|
|API Google Maps|1|
|API RRSS|1|
|Usuari|3|
|Adminisrador|3|
|Botiguer|3|
|Telerik|1|

**ESTIMACIÓ UUCW**

|Casos d'ús|Complexitat|Pes|
|---|---|---|
|Log in|Simple|5|
|Veure Newsletter|Simple|5|
|Visualitzar Ruta|Mig|10|
|Consultar rutes temàtiques|Simple|5|
|Compartir ruta visitada|Simple|5|
|Visualitzar Botiga|Mig|10|
|Valorar Botiga|Simple|5|
|Demanar gestions del sisyema|Simple|5|
|Afegir botiga|Simple|5|
|Editar Botiga|Simple|5|
|Eliminar Botiga|Simple|5|
|Gestionar notícies|Simple|5|
|Gestionar rutes temàtiques|Mig|10|

|||
|---|---|
|UUCW|35|
|UAW|12|
|TCF|0.98|
|ECF|0.98|
|UCP|45.1388|
|FP|22.5|

L'UCP ha sigut calculat usan la seguent formula: UCP = (UUCW * UAW) * TCF * ECF

UCP = (35 * 12) * 0.98 * 0.98

Un cop calculat el UCP, usan el factor PF(esforç per punt de cas d'ús) i la següent formula: Estimació temps = UCP * PF

Estimació temps = 45.1388 * 22.5 = 1015.623 hores de treball

### 2.2. Estimació de cost ###

> Calculeu el cost de personal i la resta de coses. Useu un excel o altra eina per fer els càlculs. Copieu aquí les taules (però entregueu també l'excel!). 

## 4. PLA DE FASES ##
> - a) Taula amb l'estat dels casos d'ús a cada fase

a) 

Usuari

1. Log in                             10.3 Per proximitat
2. Newsletter                         10.4 Favorites
3. Visualitzar ruta                  
4. Consultar temàtiques               Botiguer
5. Compartir ruta visitada            11. Gestions del sistema
6. Visualitzar botiga                
6.1 Consultar ofertes i descomptes    Administrador
6.2 Guardar botiga com a favorit      12. Administrar botigues
7. Compartir experiències             12.1 Afegir botigues
8. Compartir botiga                   12.2 Editar botigues
9. Valorar botigues                   12.3 Eliminar botigues
9.1 Donar puntuació                   13. Veure auditories del sistema
9.2 Fer comentari                     14. Afegir noticia
9.3 Compartir valoració               15. Administrar rutes temàtiques
10. Llistar botigues                  15.1 Afegir rutes
10.1 Per descomptes                   15.2 Editar rutes
10.2 Per tipus de botiga              15.3 Eliminar rutes
 
     Inception       Elaboration     Construction     Transition
1.   	Esboçat		Refinat         Complert        Complert
2.   	Identificat	Esboçat         Complert        Complert  
3.   	Esboçat		Analitzat       Refinat         Complert       
4.   	Identificat	Esboçat         Refinat         Complert       
5.   	Identificat	Esboçat         Refinat         Complert
6.   	Esboçat		Analitzat       Refinat         Complert
6.1  	Esboçat		Analitzat       Refinat         Complert
6.2  	Identificat     Esboçat         Refinat         Complert
7.   	Identificat     Esboçat         Refinat         Complert  
8.   	Identificat     Esboçat         Refinat         Complert
9.   	Identificat     Analitzat       Complert        Complert
9.1  	Identificat     Esboçat         Refinat         Complert       
9.2  	Identificat     Esboçat         Refinat         Complert
9.3  	Identificat	Esboçat         Refinat         Complert
10. 	Esboçat         Analitzat       Complert        Complert
10.1 	Esboçat         Analitzat       Complert        Complert
10.2 	Esboçat         Analitzat       Complert        Complert
10.3 	Esboçat         Analitzat       Complert        Complert
10.4 	Esboçat         Analitzat       Complert        Complert
11. 	Refinat         Complert        Complert        Complert
12. 	Esboçat         Analitzat       Complert        Complert
12.1 	Identificat     Esboçat         Complert        Complert
12.2 	Identificat     Esboçat         Complert        Complert
12.3 	Identificat     Esboçat         Complert        Complert
13. 	Identificat     Esboçat         Complert        Complert
14. 	Identificat     Esboçat         Complert        Complert
15.	Identificat     Esboçat         Complert        Complert
15.1 	Identificat     Esboçat         Complert        Complert
15.2 	Identificat     Esboçat         Complert        Complert
15.3 	Identificat     Esboçat         Complert        Complert
									

> - b) Informació més rellevant de cada fase. Per cada fase, dir: objectius, entregables més importants, quantes iteracions a cada fase, dates d'inici i finalització, esforç de cada rol a cada fase, etc.
