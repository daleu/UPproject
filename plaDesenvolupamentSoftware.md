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
:---:|:---:
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
:---:|:---:|:---:
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

La formula per calcular el TCF és:`TCF = 0.6 + ((Σf:f∈fTec:(pes(f) * prioritat(f))/100)/100)`

En el nostre cas obtenim que `TCF = 0.98.`

#### ESTIMACIÓ ECF ####

Factor d'Entorn|Pes|Avaluació|
:---|:---:|:---:
Capacitat analistica|0.5|3
Dificultat del llenguatge de programació|-1|2
Estabilitat dels requisits|2|3
Experiència en l'aplicació|0.5|3
Experiència en Orientació a Objectes|1|3
Familiarització amb l'UML|1.5|2
Motivació|1|2
Treball a temps parcial|-1|1

Com no es tracta de un gran sistema, dificil a implementar o complex, l'avaluació màxima que reben aquests factors es de 3 (el màxim del ECF és 5). Per tant, el més important és l'experiència i capacitat en el sector.

La formula per calcular el ECF és: `ECF = 1.4 + ‐0.03 * (Σf:f∈fEnv:(pes(f) * avaluació(f))`

En el nostre cas obtenim `ECF = 0.98`

#### ESTIMACIÓ UAW ####

Actor|Pes
:---:|:---:
API Google Maps|1
API RSS|1
Usuari|3
Adminisrador|3
Botiguer|3
Telerik|1

Necessitem actors de poca complexitat. Usuari, administrador i botiguer seria "Average" ja que necessitarem un gran nombre d'aquests actors (però tampoc exagerat). Recordem que es tracta de una aplicació senzilla d'usar i que busca ser lo més simple possible. Els altres actors, es tracten d'APIs o programari extern, per tant podrem parlar d'actors "Simple".

La formula per calcular el UAW és: `UAW = Σa:a∈actors: pes(a)`

En el nostre cas obtenim `UAW = 12`

#### ESTIMACIÓ UUCW ####

Casos d'ús|Complexitat|Pes
:---:|:---:|:---:
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
Administrar rutes temàtiques|Mig|10
LListar Botigues|Mig|10
Fer Auditories|Simple|5

No tenim casos d'ús "Complex", ja que les que comportem major esdeveniments son els usos de visualització i gestió de rutes, i aquestes són "Average" (no arriben a més de 7 esdeveniments). Recordem que es tracta de una aplicació senzilla d'usar i que busca ser lo més simple possible. Els altres casos d'ús són "Simple" ja que desenvolupen 1 o 2 esdeveniments com a màxim.

La formula per calcular el UUCW és: `UUCW = Σc:c∈casosÚs:pes(c)`

En el nostre cas obtenim `UUCW = 110`

#### UCP ####

Factor|Resultat
:---:|:---:
UUCW|110
UAW|12
TCF|0.98
ECF|0.98

La formula per calcular el UCP és: `UCP = (UUCW * UAW) * TCF * ECF`

En el nostre cas obtenim `UCP = 117.1688`

Per obtenir l'Estimació del temps, un cop calculat el UCP, usan el factor PF(esforç per punt de cas d'ús) i la següent formula:`Estimació temps = UCP * PF`

En el nostre cas obtenim Estimació Temps = 1988.028 hores de treball ja que fem servir un `FP =  22.5`

### 2.2. Estimació de cost ###

#### Dedicacions previstes per rol ####

Rol|Inception|Elaboration|Construction|Transition
:---|:---:|:---:|:---:|:---:
Cap de projecte|19.00%|12.00%|12.00%|60.00%
Arquitecte|10.00%|15.00%|12.00%|6.67%
Analista funcional|35.00%|25.00%|5.00%|6.67%
Analista de xarxes|3.00%|10.00%|7.00%|6.67%
Dissenyador|30.00%|17.00%|5.00%|6.67%
Administrador de Base de Dades|3.00%|10.00%|12.00%|6.67%
Programador Senior|0.00%|8.00%|35.00%|6.67%
Tester|0.00%|3.00%|12.00%|0.00%

Per cada fase s'ha establert un percentatge de dedicació per cada rol necessari. Aquesta dedicació s'usara per calcular el factor de treball.

#### Salari previst per rol ####

Rol|Salari/hora|Factor de treball|Hores de treball|Salari en net|Salari en brut|
---|:---:|:---:|:---:|:---:|:---:|
Cap de projecte|14€|20%|524.6237|29,379€|41,130€
Arquitecte|12€|12%|313.7197|15,059€|21,082€
Analista funcional|12€|14%|375.67275|18,032€|25,245€
Analista de xarxes|12€|7%|196.40435|9,427€|13,198€
Dissenyador|10€|11%|299.22005|11,969€|16,756€
Administrador de Base de Dades|10€|10%|255.7211|10,229€|14,320€
Programador Senior|12€|19%|504.85145|24,233€|33,926€
Tester|6€|0.104|6%|166.0869|3,986€|5,581€

Considerem el Cap de projecte el rol de més pes del equip. Seguit per l'Arquitecte, Analista funcional, Analista de xarxes i Programador Senior. Aquests són essencials perquè el sistema es desenvolupi ràpid i bé. Després tindriem el Administrador de Bases de Dades i el Dissenyador, només són essencials per un factor en concret. Per últim quedaria el Tester de l'aplicació, el qual és necessari però no desenvolupa un servei d'especialista.

El factor de treball surten de la ponderació de cada rol amb les arees.

El factor de treball surt al multiplicar el factor de treball per les hores totals del projecte.

El salari brut s'obté a partir de la formula `Salari en brut = Salari/hora * Hores de treball`

El salari net s'obté a partir de la formula `Salari en net = Salari en brut - Salari en brut * 0.4 `

#### LLista de costos ####

|Llista de costos|Preu|
|:---:|:---:|
|Costos del personal|178,417€|
|Cost del lloc de treball|2.800€|
|Cost total del personal|180,017€|
|Despeses estructurals|10,104€|
|Percentatge del marge de benefici|30,985€|
|Percentatge de contingències (Riscos)|10,845€|

Els costos de personal surten de la suma de tots els salaris del equip de treball.

El cost de treball es fixe, 200€ per empleat.

El cost total del personal, es la suma del cost del personal mab el del lloc de treball.

Les despes estructurals les obtenim amb la formula: `Cost toal de personal * 0.15`

El percentatge del marge de benefici l'obtenim  amb la formula: `(Cost total del personal + Despases estructurals) * 0.4`

El percentat de contingències (Riscos) l'obtenim amb la formula: `(Cost total del personal + Despases estructurals + Percentatge del marge de benefici) * 0.1`

El pressupost final es la suma de tots els costos, per tant obtenim: `Pressupost final: 323,735€`

## 3. PLA DE FASES ##

###3.1 Estats de casos d'ús

|Casos d'ús| |
|---|---|
|1 - Log in|10.3 - Per proximitat|
|2 - Newsletter|10.4 - Favorites|
|3 - Visualitzar ruta| |                  
|4 - Consultar temàtiques|Botiguer|
|5 - Compartir ruta visitada|11 - Gestions del sistema|
|6 - Visualitzar botiga| |                
|6.1 - Consultar ofertes i descomptes|Administrador|
|6.2 - Guardar botiga com a favorit|12 - Administrar botigues|
|7 - Compartir experiències|12.1 - Afegir botigues|
|8 - Compartir botiga|12.2 - Editar botigues|
|9 - Valorar botigues|12.3 - Eliminar botigues|
|9.1 - Donar puntuació|13 - Veure auditories del sistema|
|9.2 - Fer comentari|14 - Afegir noticia|
|9.3 - Compartir valoració|15 - Administrar rutes temàtiques|
|10. - Llistar botigues|15.1 - Afegir rutes|
|10.1 - Per descomptes|15.2 - Editar rutes|
|10.2 - Per tipus de botiga|15.3 - Eliminar rutes|
 
|Num|Inception|Elaboration|Construction|Transition|
|---|---|---|---|---|
|1.|Esboçat|Refinat|Complert|Complert|
|2.|Identificat|Esboçat|Complert|Complert|  
|3.|Esboçat|Analitzat|Refinat|Complert|       
|4.|Identificat|Esboçat|Refinat|Complert|       
|5.|Identificat|Esboçat|Refinat|Complert|
|6.|Esboçat|Analitzat|Refinat|Complert|
|6.1|Esboçat|Analitzat|Refinat|Complert|
|6.2|Esboçat|Analitzat|Refinat|Complert|
|7.|Identificat|Esboçat|Refinat|Complert|  
|8.|Identificat|Esboçat|Refinat|Complert|
|9.|Identificat|Esboçat|Refinat|Complert|
|9.1|Identificat|Esboçat|Refinat|Complert|       
|9.2|Identificat|Esboçat|Refinat|Complert|
|9.3|Identificat|Esboçat|Refinat|Complert|
|10.|Identificat|Analitzat|Complert|Complert|
|10.1|Esboçat|Analitzat|Complert|Complert|
|10.2|Esboçat|Analitzat|Complert|Complert|
|10.3 |Esboçat|Analitzat|Complert|Complert|
|10.4 |Esboçat|Analitzat|Complert|Complert|
|11.|Refinat|Complert|Complert|Complert|
|12.|Esboçat|Analitzat|Complert|Complert|
|12.1|Identificat|Esboçat|Complert|Complert|
|12.2|Identificat|Esboçat|Complert|Complert|
|12.3|Identificat|Esboçat|Complert|Complert|
|13.|Identificat|Esboçat|Complert|Complert|
|14.|Identificat|Esboçat|Complert|Complert|
|15.|Identificat|Esboçat|Complert|Complert|
|15.1|Identificat|Esboçat|Complert|Complert|
|15.2|Identificat|Esboçat|Complert|Complert|
|15.3|Identificat|Esboçat|Complert|Complert|

									

###3.1 Informació rellevant

A partir del grau d'esforç de cada treballador amb diferent rol y les hores que cadascú ha de treballa ens dona el següent esforç i durada de cada fase del projecte.

|Inception|Elaboration|Construction|Transition
:---:|:---:|:---:|:---:|:---:
Effort	|5%|25%|55%|15%
Schedule|10%|25%|45%|20%

Per aquesta taula hem sigut els patrons d'una estimació standard però li hem aplicat unes petites modificacions per adaptar-lo al nostre projecte.

* Per una banda pel que es fa respecte al **effort**, hem  considerat que es necesita més esforç a la fase de *Elaboration  i Contruction*. Ja que l'èxit de la nostra app dependrà sobretot de la validesa, simplicitat y funcionals dades obtingutes dels comerços. Llavors a cada fase s'haurà d'afegir un esforç extra d'un seguiment sobre les dades obtingudes, si existeixen dificultats, si s'haurien d'afegir més funcionalitats, ect. Però sobretot amb el pas del temps saber com evoluciona aquest estat de les dades.
* Per l'altre banda, pel que fa a la part de **schedule** va molt lligat a la mateixa raó pel qual s'ha modificat l'**effort**. Ja que es necessitarà a les mateixes fases citades anteriorment un temps afegit als projectes standart en la recollida de dades y gestió d'aquestes.

Per tant a partir d'aquest patró d'esforç i temps destinat al projecte ens surtens aquestes dates de finalizació de fase i el temps que s'haurà de destinar a cadascuna, suposant de que el projecte es va iniciar el día **1 de Febrer**.

|Inception|Elaboration|Construction|Transition
:---:|:---:|:---:|:---:|:---:
Dies Laborables|5|12|22|10
Data Límit|8 de Febrer|24 de Febrer|30 de Març|13 de Abril
Esforç (hores)|198,8 |497|894,6|397,6

###3.1.1 Síntesis de les iteracions de cada fase

#### 1.Inception
Iteració| DataIni| DataFi |Staff
:---:|:---:|:---:|:---:|
 T1|1 de Febrer|5 de Febrer| 0.1

###### Objectius principals
1. Establir el model de projecte
2. Definir visió del projecte
3. Estimar el temps i calcular pressupost
4. Esmentar els possibles ricos
5. Disenyar els casos d'ús i funcionalitats

#### 2.Elaboration
Iteració| DataIni| DataFi |Staff
:---:|:---:|:---:|:---:|
E1|8 de Febrer|16 de Febrer| 0.3

###### Objectius principals
1. Preparació i comprobació de l'entorn de treball
2. Implementar casos d'ús més important
3. Fer pla de com recollir les dades
4. Disenyar els casos d'ús i funcionalitats
5. Dissenyar l'estructura de la base de dades
6. Validar requisits

Iteració| DataIni| DataFi |Staff
:---:|:---:|:---:|:---:|
E2|17 de Febrer|23 de Febrer| 0.3

###### Objectius principals
1. Mitigar riscos arquitectònics
2. Iniciar a recollir dades per veure efectivitat
3. Establir l'entorn de treball definitiu

#### 3.Construction
Iteració| DataIni| DataFi |Staff
:---:|:---:|:---:|:---:|
C1|24 de Febrer|4 de Març| 0.45

###### Objectius principals
1. Descriure casos d'ús adicionals
2. Implementar casos d'ús
3. Recollir dades de manera més optimitzada

Iteració| DataIni| DataFi |Staff
:---:|:---:|:---:|:---:|
C2|7 de Març|16 de Març| 0.45

###### Objectius principals
1. Idem
2. Fer un seguimenta de la funcionalitat i practicitat

Iteració| DataIni| DataFi |Staff
:---:|:---:|:---:|:---:|
C3|17 de Març|29 de Març|0.45

###### Objectius principals
1. Idem
2. Crear una versió beta per a l'úsuari i rol de botiguer
3. Obtenir la valoració de posibles usuaris

#### 4.Transition
Iteració| DataIni| DataFi |Staff
:---:|:---:|:---:|:---:|
C1|30 de Març|12 de Abril|0.15

###### Objectius principals
1. Descriure casos d'ús adicionals
2. Implementar casos d'ús
3. Recollir dades de manera més optimitzada
