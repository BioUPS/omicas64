# Otros datasets y posibles pipelines sugeridos:

1. NCBI >> SRR2584863  
📌 Tema: Ensamblaje y anotación.  
🧪 Pipeline sugerido  
FASTQ → QC → trimming → ensamblaje → anotación  
  
2. NCBI >> SRR1976948  
📌 Tema: Diversidad microbiana intestinal.  
🧪 Pipeline sugerido  
FASTQ → filtrado → QIIME2 → taxonomía → gráficos   

3. NCBI >> SRR12529581  
📌 Tema: Detección de variantes virales SARS-CoV-2  
🧪 Pipeline sugerido  
FASTQ → trimming → BWA → samtools → variantes    

4. NCBI >> SRR1976948  
📌 Tema: Secuenciación de tercera generación (Ensamblaje).  
🧪 Pipeline sugerido  
FASTQ → NanoPlot → Flye → Medaka → control    

5. NCBI >> SRR2584863   
📌 Tema: Evolución experimental en Escherichia coli.  
🧪 Pipeline sugerido  
FASTQ → FastQC → trimming → BWA contra referencia → samtools → variant calling → interpretación de SNPs/indels   

6. NCBI >> SRR1553607  
📌 Tema: Genómica viral: Zaire ebolavirus.  
🧪 Pipeline sugerido  
FASTQ → FastQC → trimming → mapeo contra referencia viral → samtools → consenso → variantes  

## Puede usar tutoriales para guiarse y trabajar sobre estas secuencias.
