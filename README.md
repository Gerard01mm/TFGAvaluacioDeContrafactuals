# Treball Final de Grau: Avaluació amb usuaris d’explicacions contrafactuals comparant el format tabular i el format textual

## Introducció
Aquest repositori compta amb tot el programari que s'ha utilitzat per a preparar el classificador binari. Aquest classificador binari s'encarrega, en primer lloc, de classificar una sol·licitud de crèdit en denegat o concedit segons les característiques de la sol·licitud introduida. Però, a més, per a aquelles sol·licituds de crèdit que s'han classificat com a denegades, el sistema genera un seguit de contrafactuals per a poder indicar possibles canvis a fer per a la sol·licitud de crèdit per a que aquesta canviï la seva classificació a concedit.

## Eines utiltizades en la preparació
Les eines utilitzades per a la preparació d'aquest projecte ha estat:

- Anaconda Navigator: utilitzat per a preparar l'entorn i així evitar incompatibilitats amb altres llibreries de Python.
- Jupyter Notebook: utilitzat com a editor per al fitxer notebook, on es troba la implementació del codi.
- AIX360: llibreria utilitzada en aquesta preparació per poder crear les explicacions contrafactuals.
- SKlearn: llibreria utilitzada per a instanciar el model darrere el classificador binari.

## Instruccions per a executar el notebook important l'entorn
Per a poder executar el fitxer notebook, primer cal fer certes preparacions a l'entorn de desenvolupament on executarem el notebook. Per això, a la carpeta /BackUps/ podem trobar un fitxer **backUpNNContrastive.yaml** que al descarregar-lo, podem importar l'entorn complert per a executar el notebook. 

Per fer això utilitzant Anaconda Navigator:

1. Ens dirigirem a la finestra principal d'anaconda icercarem al menú situat a l'esquerra l'opció **environments**
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar1.png">

2. En el menú on es llistaràn tots els entorns creats, a la part inferior trobarem un menú amb 5 butons. Si polsem el botó **import**, ens apareixerà una finestra pop up.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar2.png">

3. Seleccionarem la opció **local drive** i polsarem a la carpeta al costat de la textbox. Se'ns obrirà l'explorador d'arxius i haurem de cercar l'ubicació on s'ha descarregat el fitxer .yaml.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar3.png">

4. Un cop seleccionem el fitxer .yaml descarregat anteriorment, polsarem el botó **Import** de la finestra i l'entorn es començara a clonar.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar4.png">

5. Un cop importat l'entorn, haurem de realitzar la instal·lació de AIX360. Per això, tornarem al llistat d'entorns i polsarem el botó **play** de l'entorn importat i posteriorment polsarem **Open terminal**+
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar5.png">

6. A la terminal que se'ns aparegui, ens desplacarem fins a la ubicació on tinguem el notebook **BinaryClassificator.ipynb**. Un cop estem en aquest directori, executarem la comanda _git clone https://github.com/Trusted-AI/AIX360_.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar6.png">

7. Un cop s'hagi clonat el repositori, a la ubicació actual s'haurà creat una carpeta **AIX360**. Des de la terminal accedim a aquesta carpeta i, donat que en el notebook s'utilitza el mètode **NNContrastive**, haurem d'executar la comanda _pip install -e .[nncontrastive]_.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar7.png">

Un cop hagi finalitzat la resolució de dependències, el notebook ja es podrà executar.

## Instruccions per a executar el notebook creant de 0 l'entorn
Però, en cas que es produeixi un error, o en cas de voler-lo fer de 0, es poden seguir els passos següents:

1. Primer, s'ha de crear un entorn de desenvolupament amb Anaconda Navigator. Primer, ens adreçarem de nou a la pestanya de **Environments** des de el menú inicial d'Anaconda.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/tutorialImportar/importar1.png">

2. En el menú inferior, polsarem el botó **Create**.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/TutorialCrearEntorn/Crear2.png">

3. En el moment de pulsar el boto, s'obrirà una finestra pop up, on introduirem un nom per a l'entorn i posteriorment seleccionarem la CheckBox de Python i, per utilitzar l'explicador nncontrastive, la versió de Python haura de ser una versió **3.10.X**.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/TutorialCrearEntorn/Crear3.png">

4. El següent pas serà instal·lar les llibreries necessaries. Per això, accedirem a la terminal del nou entorns (el qual apareixerà a la llista d'entorns) polsant el botó **play** de l'entorn i posteriorment a **Open terminal**.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/TutorialCrearEntorn/Crear4.png">

5. Un cop a la terminal, primer instal·larem tot l'entorn de jupyter per poder utilitzar Jupyter Notebook. Introduirem a la terminal la comanda _pip install jupyter_
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/TutorialCrearEntorn/Crear5.png">

6. Un cop finalitzat el procés anterior, clonarem el repositori de la llibreria AIX360. La clonació d'aquest repositori haurà de realitzar-se a la mateixa ubicació que el fitxer **BinaryClassifier.ipynb**, ja que en qualsevol altre cas, el notebook no detectarà la llibreria AIX360. La comanda que s'utilitzarà serà _git clone https://github.com/Trusted-AI/AIX360_
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/TutorialCrearEntorn/Crear6.png">

7. En el mateix directori que el punt 6, ens apareixerà una carpeta anomenada **AIX360**, amb la comanda _cd_ accedirem a aquesta carpeta i, com en aquest projecte s'ha utilitzat el mètode **NNContrastiveExplainer**, la comanda que haurem d'executar dins de la carpeta **AIX360** serà _pip install -e .[nncontrastive]_. Amb aquesta comanda, totes les dependencies s'instal·laran automàticament.
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/TutorialCrearEntorn/Crear7.png">

8. L'ultim paquet que s'instal·larà serà joblib, una llibreria que ens permet emmagatzemar un model ja entrenat en un fitxer per evitar entrenar en cada execució. Per instal·lar aquesta llibreria, caldrà executar la comanda _pip install joblib_
<img src="https://github.com/Gerard01mm/TFGAvaluacioDeContrafactuals/blob/main/TutorialCrearEntorn/Crear8.png">

Un cop hagi acabat la instal·lació de la llibreria, el notebook ja serà capaç d'importar les llibreries sense donar cap error. Ara, per poder executar les cel·les sense problemes, hem de seguir els següents pasos:

1. (Opcional) Descarregar el fitxer situat al directori del repositori /TrainedModel, on es trobarà un fitxer .joblib, que conté el model ja entrenat. En cas de voler entrenar un altre model, no cal descarregar aquest fitxer.
2. Descarregar la carpeta /archive/german_credit_data.csv i introduir aquesta carpeta en el mateix directori que es trobi el notebook. **Si el fitxer german_credit_data.csv es posa en una ubicació que no sigui en una carpeta _archive_, i aquesta carpeta no es troba en la mateixa ubicació que el fitxer notebook, el fitxer notebook no podrà trobar les dades i retornarà error** 

Un cop seguits aquests pasos, ja es pot començar a executar les cel·les del notebook sense cap tipus de problema.

