# Treball Final de Grau: Avaluació amb usuaris d’explicacions contrafactuals comparant el format tabular i el format textual

### Introducció
Aquest repositori compta amb tot el programari que s'ha utilitzat per a preparar el classificador binari. Aquest classificador binari s'encarrega, en primer lloc, de classificar una sol·licitud de crèdit en denegat o concedit segons les característiques de la sol·licitud introduida. Però, a més, per a aquelles sol·licituds de crèdit que s'han classificat com a denegades, el sistema genera un seguit de contrafactuals per a poder indicar possibles canvis a fer per a la sol·licitud de crèdit per a que aquesta canviï la seva classificació a concedit.

### Eines utiltizades en la preparació
Les eines utilitzades per a la preparació d'aquest projecte ha estat:

- Anaconda Navigator: utilitzat per a preparar l'entorn i així evitar incompatibilitats amb altres llibreries de Python.
- Jupyter Notebook: utilitzat com a editor per al fitxer notebook, on es troba la implementació del codi.
- AIX360: llibreria utilitzada en aquesta preparació per poder crear les explicacions contrafactuals.
- SKlearn: llibreria utilitzada per a instanciar el model darrere el classificador binari.

### Instruccions per a la seva preparació
Per a poder executar el fitxer notebook, primer cal fer certes preparacions a l'entorn de desenvolupament on executarem el notebook. Per això, a la carpeta /BackUps/ podem trobar un fitxer **backUpNNContrastive.yaml** que al descarregar-lo, podem importar l'entorn complert per a executar el notebook. Per fer això utilitzant Anaconda Navigator, ens dirigirem a la finestra principal d'anaconda, cercarem al menú situat a l'esquerra l'opció **environments** i en el menú on es llistaràn tots els entorns creats, a la part inferior trobarem un menú amb 5 butons. Si polsem el botó import, ens apareixerà una finestra pop up on seleccionarem la opció **local drive** i polsarem a la carpeta al costat de la textbox. Se'ns obrirà l'explorador d'arxius i haurem de cercar l'ubicació on s'ha instal·lat l'entorn. Un cop seleccionem el fitxer .yaml descarregat anteriorment, polsarem el botó **Import** de la finestra i l'entorn es començara a clonar.

Però, en cas que es produeixi un error, o en cas de voler-lo fer de 0, es poden seguir els passos següents:

1. Primer, s'ha de crear un entorn de desenvolupament amb Anaconda NAvigator. Aquest entorn ha de contenir: Python 3.10, l'entorn complert de jupyter per poder utilitzar Jupyter Notebook
2. Per a poder utilitzar AIX360 en aquest entorn, en un directori a part, s'haura de clonar el repositori de AIX360 amb la següent comanda: git clone https://github.com/Trusted-AI/AIX360
3. Posteriorment, en una consola amb l'entorn creat al punt 1 activat, s'haurà d'executar la següent comanda: pip install -e .[nncontrastive].


Un cop hagi acabat la instal·lació de la llibreria, ja es podrà començar a utilitzar la llibreria. Ara, per poder executar les cel·les sense problemes, hem de seguir els següents pasos:

1. (Opcional) Descarregar el fitxer situat al directori del repositori /TrainedModel, on es trobarà un fitxer .joblib, que conté el model ja entrenat. En cas de voler entrenar un altre model, no cal descarregar aquest fitxer.
2. Descarregar la carpeta /archive/german_credit_data.csv i introduir aquesta carpeta en el mateix directori que es trobi el notebook. **Si el fitxer german_credit_data.csv es posa en una ubicació que no sigui en una carpeta _archive_, i aquesta carpeta no es troba en la mateixa ubicació que el fitxer notebook, el fitxer notebook no podrà trobar les dades i retornarà error** 

Un cop seguits aquests pasos, ja pots començar a executar les cel·les del notebook sense cap tipus de problema.
