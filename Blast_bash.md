#BLASTing a una base de datos de proteínas

Para instalar en el terminal:
~~~
$ sudo apt install ncbi-blast+
~~~

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
 
4. Crear una base de datos con el siguiente comando:
~~~
$ makeblastdb -in swissprot.fa -input_type fasta -title swissprot -dbtype prot
~~~
 
* Puede averiguar opciones para ejecutar este comando:
~~~
$ makeblastdb -help
~~~

5. Descargar la información de la secuencia de proteínas para BRCA1 humano. Guardelo con el nombre de archivo "brca1_pep.fa" (mv).
[secuencia_BRCA1](https://raw.githubusercontent.com/BioUPS/omicas64/main/BRCA1%20%5BHomo%20sapiens%5D.fasta)
Puede crear el archivo brca1, copiando la secuencia, usando:
~~~
$ nano brca1_pep.fasta
~~~
6. Realizar la búsqueda con BLASTp en el archivo brca1 pep.fasta, creado en el paso anterior.
~~~
$ blastp -query brca1_pep.fasta -db swissprot.fa > brca1_swissprot
~~~
7. Revise los resultados, qué información nos proveen. 
~~~
$ less brca1_swissprot
~~~
¿Cuáles son los mejores alineamientos?
