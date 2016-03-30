# BotiguesBCN - PLA DE DESENVOLUPAMENT DE SOFTWARE #

## 1. ORGANITZACIÓ I EQUIP ##

El sistema BotiguesBCN ha de ser senzill, eficaç i agradable d’usar. El nostre projecte consisteix en el desenvolupament i manteniment de una aplicació mòvil i web, per tant, el nostre equip haurà de ser especialista en aquest àmbit.
El nostre equip de treball estara organitzat respecte la seva funció sobre el desenvolupament, manteniment i supervisió del sistema.
Distingirem entre els seguents rols de treball:

* Cap del projecte. Es la persona responsable de gestionar el projecte. Es necessita de molta experiència i coneixements en el camp dels projectes.
* Arquitecte (Cap Tècnic). Es la persona responsable de crear un entorn de treball on la gent es trobi a gust i autoritzada per fer qualsevol de les seves tasques o responsabilitats.
* Dissenyador. Es la persona encarregada de transformar els requisits del usuari en un disseny arquitectònic que proveira d'especificacions als programadors.
* Programador Senior. Programador amb expert i especialista. Té un nivell de programació experta en el seu camp i una capacitat de treball alt.
* Analista Funcional. Es la persona responsable de supervisar el desenvolupament de la aplicació mòvil i web. Assegurant-se la màxima explotació del entorn i que disposi de un rediment òptim.
* Analista de Xarxes. Es la persona responsable de dissenyar i gestionar la seguretat de la Xarxa que usara l'aplicació.
* Administrador Base de Dades. Es la persona responsable dels aspectes d'entorn de la Base de Dades que utilitzara l'aplicació.
* Tester. Es la persona responsable de realitzar proves a l'aplicació i reporta els seus errors abans de la sortida d'aquesta al públic.

Rol|Persones
---|---
Cap del projecte|1
Arquitecte|1
Dissenyador|1
Programador Senior|2
Analista Funcional|1
Analista de Xarxes|1
Administrador Base de Dades|1
Tester|10

## 2. PLA DE PROJECTE ##

### 2.1. Estimació d'esforç ###

#### ESTIMACIÓ TCF ####

Descripció|Pes|Prioritat
---|---|---
Sistema distribuït|1|5
Rendiment|2|3
Eficiencia del Usuari Final|2|5
Processamet intern complex|0.5|1
Reusabilitat|1|4
Fàcil de instalar|-1|5
Fàcil d'usar|0.5|5
Portabilitat|0.5|4
Fàcil de canviar|2|3
Característiques especials de seguretat|1|5
Accés directe desde tercers|1|5
Es necessiten usuaris experts o entrenats|-1|3



Considerem essencial que BotiguesBCN sigui un sistema segur, fàcil d'usar, distribuit i accesible, això es degut a que hem de conseguir la màxima satisfacció del usuari. Com es tracta de un sistema senzill no li donem importància al processament intern. Els altres factors els considerem amb prioritat "normal" (2, 3 i 4).

La formula per calcular el TCF és:`TCF = 0.6 + ((Σf:ffTec:(pes(f) * prioritat(f))/100)/100)`

En el nostre cas obtenim que `TCF = 0.98.`

#### ESTIMACIÓ ECF ####

Factor d'Entorn|Pes|Avaluació|
---|---|---
Capacitat analistica|0.5|3
Dificultat del llenguatge de programació|-1|2
Estabilitat dels requisits|2|3
Experiència en l'aplicació|0.5|3
Experiència en Orientació a Objectes|1|3
Familiarització amb l'UML|1.5|2
Motivació|1|2
Treball a temps parcial|-1|1

Com no es tracta de un gran sistema, dificil a implementar o complex, l'avaluació màxima que reben aquests factors es de 3 (el màxim del ECF és 5). Per tant, el més important és l'experiència i capacitat en el sector.

La formula per calcular el ECF és: `ECF = 1.4 + ‐0.03 * (Σf:ffEnv:(pes(f) * avaluació(f))`

En el nostre cas obtenim `ECF = 0.98`

#### ESTIMACIÓ UAW ####

Actor|Pes
---|---
API Google Maps|1
API RSS|1
Usuari|3
Adminisrador|3
Botiguer|3
Telerik|1

Necessitem actors de poca complexitat. Usuari, administrador i botiguer seria "Average" ja que necessitarem un gran nombre d'aquests actors (però tampoc exagerat). Recordem que es tracta de una aplicació senzilla d'usar i que busca ser lo més simple possible. Els altres actors, es tracten d'APIs o programari extern, per tant podrem parlar d'actors "Simple".

La formula per calcular el UAW és: `UAW = Σa:aactors: pes(a)`

En el nostre cas obtenim `UAW = 12`

#### ESTIMACIÓ UUCW ####

Casos d'ús|Complexitat|Pes
---|---|---
Log in|Simple|5
Veure Newsletter|Simple|5
Visualitzar Ruta|Mig|10
Consultar rutes temàtiques|Simple|5
Compartir ruta visitada|Simple|5
Visualitzar Botiga|Mig|10
Valorar Botiga|Simple|5
Demanar gestions del sisyema|Simple|5
Afegir botiga|Simple|5
Editar Botiga|Simple|5
Eliminar Botiga|Simple|5
Gestionar notícies|Simple|5
Gestionar rutes temàtiques|Mig|10

No tenim casos d'ús "Complex", ja que les que comportem major esdeveniments son els usos de visualització i gestió de rutes, i aquestes són "Average" (no arriben a més de 7 esdeveniments). Recordem que es tracta de una aplicació senzilla d'usar i que busca ser lo més simple possible. Els altres casos d'ús són "Simple" ja que desenvolupen 1 o 2 esdeveniments com a màxim.

La formula per calcular el UUCW és: `UUCW = Σc:ccasosÚs:pes(c)`

En el nostre cas obtenim `UUCW = 35`

#### UCP ####

|
---|---
UUCW|35
UAW|12
TCF|0.98
ECF|0.98
FP|22.5

La formula per calcular el UCP és: `UCP = (UUCW * UAW) * TCF * ECF`

En el nostre cas obtenim `UCP = 45.1388`

Per obtenir l'Estimació del temps, un cop calculat el UCP, usan el factor PF(esforç per punt de cas d'ús) i la següent formula:`Estimació temps = UCP * PF`

En el nostre cas obtenim Estimació Temps = 1015.623 hores de treball ja que fem servir un `FP =  22.5`

### 2.2. Estimació de cost ###

#### Dedicacions previstes per rol ####

Disciplina|Rol|Dedicació|Rol|Dedicació|Rol|Dedicació|Factor d'importancia
---|---|---|---|---|---|---|---
Model d'empresa|Arquitecte|80%|Cap de Projecte|20%|13
Requeriments|Analista de Xarxes|40%|Cap de Projecte|20%|Analista funcional|40%|18
Anàlisis i disseny|Dissenyador|50%|Analista funcional|30%|Analista de Xarxes|20%|20
Implementació|Analista funcional|25%|Programador Senior|55%|Administrador de BD|20%|18
Test|Tester|80%|Programador|Senior|10%|Administrador de BD|10%|13
Project|Manager|Cap de projecte|100%|18

#### Salari previst per rol ####

|Rol|Salari/hora|Factor de treball|Hores de treball|Salari en net|Salari en brut|
|---|---|---|---|---|---|
|Cap de projecte|14€|0.242|245.78246|13,764€|19,269€|
|Arquitecte|12€|0.104|105.62552|5,070€|7,098€|
|Analista funcional|12€|0.177|179.76651|8,629€|12,080€|
|Analista de xarxes|12€|0.112|113.75056|5,460€|7,644€|
|Dissenyador|10€|0.1|101.563|4,063€|5,688€|
|Administrador de Base de Dades|10€|0.049|49.76587|1,991€|2,787€|
|Programador Senior|12€|0.112|113.75056|5,460€|7,644€|
|Tester|6€|0.104|105.62552|2,535€|3,549€|

Considerem el Cap de projecte el rol de més pes del equip. Seguit per l'Arquitecte, Analista funcional, Analista de xarxes i Programador Senior. Aquests són essencials perquè el sistema es desenvolupi ràpid i bé. Després tindriem el Administrador de Bases de Dades i el Dissenyador, només són essencials per un factor en concret. Per últim quedaria el Tester de l'aplicació, el qual és necessari però no desenvolupa un servei d'especialista.

El salari brut s'obté a partir de la formula `Salari en brut = Salari/hora * Hores de treball`

El salari net s'obté a partir de la formula `Salari en net = Salari en brut - Salari en brut * 0.4 `

#### LLista de costos ####

|Llista de costos|Preu|
|---|---|
|Costos del personal|65,759€|
|Cost del lloc de treball|1,600€|
|Cost total del personal|67,359€|
|Despeses estructurals|10,104€|
|Percentatge del marge de benefici|30,985€|
|Percentatge de contingències (Riscos)|10,845€|

Pressupost final: 120,893€

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
