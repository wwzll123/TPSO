# TPSO-DBP
Standalone Program of TPSO-DBP
# Pre-requisite:
- Python, java,numpy, pytorch
- SANN software (https://github.com/newtonjoo/sann)
- NCBI nr90 database (ftp://ftp.ncbi.nlm.nih.gov/blast/db/FASTA/)
- PSIPRED software(https://i12r-studfilesrv.informatik.tu-muenchen.de/wiki/index.php/Psipred)
- Linux system (suggested CentOS 7)
# Installation:
First,download compressed package.
second, uncompress it.
third,provide executable permissions for file of './jar/tools/blast-2.2.26/blastpgp'.


# Set config
The files of “Config.properties” and "config.ini" should be set as follows:

* Config.properties
 ```
DBS_PRED_MODEL=./jar/model/dbs/dbs.mod
BLAST_BIN_DIR=./jar/tools/blast-2.2.26
BLASTPGP_EXE_PATH=./jar/tools/blast-2.2.26/blastpgp

#Need change
SANN_RUNNER_PATH=Absolute_Path_SANN_Installtion/SANN/sann/bin/sann.sh
BLASTPGP_DB_PATH=Absolute_Path_nr_Installtion/nr
```
* config.ini
 ``` 
[PATH]

#Need change
TPSO_HOME=/data0/junh/stu/wenwuzeng/software/TPSO_DBP
PSIPRED_HOME=Absolute_Path_PSIPRED_Installtion/psipred321
 ```
 
 # Running
You should make sure your query protein seqs in the file of './workFolder/seqs.fa'.
than, enter the following command lines on Linux System.
 ``` 
 python main.py
``` 
the predicted result will be generated in file of './workFolder/seqs.fa'.
  
# Note
- Files of .dbs_prob, .sa and .opssm are generated in './jar/example'.
- The .ss file is generated by PSIPRED generated in './workFolder'.
- If you already have these files, just put them into the corresponding folder, then the feature generator will not run. This will greatly reduce the prediction time.
- If you have any question, please send email to z804908905@163.com.
- All the best to you!
 
