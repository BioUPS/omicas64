#BLASTing a una base de datos de proteínas

1. Contruir una base de datos. En una carpeta llamada "blast" (mkdir), descargue la base de datos Swissprot de NCBI con el siguiente comando:

~~~
$ wget ftp://ftp.ncbi.nih.gov/blast/db/FASTA/swissprot.gz
~~~

2. Descomprimir el archivo descargado con el siguiente comando:

~~~
 $ gunzip swissprot.gz
~~~
 
3. Cambiar el nombre del archivo, aunque no existe una extensión de archivo, el archivo es un archivo FASTA. 
~~~
$ mv swissprot swissprot.fa
~~~
 
4. Crear una base de datos con el siguiente comando:ls
~~~
$ makeblastdb -in swissprot.fa -input_type fasta -title swissprot -dbtype prot
~~~
 
* Puede averiguar opciones para ejecutar este comando:
~~~
$ makeblastdb -help
~~~

5. Descargar la información de la secuencia de proteínas para BRCA1 humano. Guardelo con el nombre de archivo "brca1_pep.fa" (mv).
 Abra la secuencia con:

$ nano brca1_pep.fasta

Para guardar con nano, escriba Ctrl-X, luego escriba Y. A continuación, podemos EXPLOTAR el archivo brca1 pep.fasta que creamos.

$ blastp -query brca1_pep.fasta -db swissprot.fa > brca1_swissprot

 

¿Tienen sentido para ti los mejores éxitos? Puede buscar en NCBI Protein algunas de las identificaciones.

$ less brca1_swissprot

 

¿Cuáles son los mejores éxitos? ¿Tiene sentido el orden de las secuencias en términos de lo que sabes de biología?

También puede hacer BLAST la secuencia en la base de datos “no redundante” “nr” pegándola en la herramienta web NCBI BLAST: https://blast.ncbi.nlm.nih.gov/Blast.cgi . Tenga en cuenta que, en teoría, podría hacer esto especificando “nr” para la base de datos, pero muchos servidores no lo tienen descargado (¡es un archivo muy grande!).

