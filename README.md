#Fusarium comparative genomics

##Directory structure
Run the build_dir.pl script to make a directory structure
Usage: build_dir.pl <projectname.csv>
where the csv is a comma delimited file with the following:
DNA,PE,fusarium_comp,various
```
/home/harrir/git_master/seq_tools/directory_structure/build_dir.pl /home/harrir/projects/git_projects/fusarium_comp/fusarium_comp.csv 
```
Now copy the reads into the comparative genomics directory

```
RawDatDir=/home/groups/harrisonlab/raw_data/raw_seq/fusarium/HAPI_seq_3/ 
    ProjectDir=/home/groups/harrisonlab/project_files/fusarium_comp
    mkdir -p $ProjectDir/raw_dna/paired/F.proliferatum/A8/F
    mkdir -p $ProjectDir/raw_dna/paired/F.proliferatum/A8/R
    mkdir -p $ProjectDir/raw_dna/paired/F.oxysporum_fsp_narcissi/N139/F
    mkdir -p $ProjectDir/raw_dna/paired/F.oxysporum_fsp_narcissi/N139/R
    mkdir -p $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG3/F
    mkdir -p $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG3/R
    mkdir -p $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG18/F
    mkdir -p $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG18/R

cp $RawDatDir/Fproliferatum_S1_L001_R1_001.fastq.gz $ProjectDir/raw_dna/paired/F.proliferatum/A8/F/.
    cp $RawDatDir/Fproliferatum_S1_L001_R2_001.fastq.gz $ProjectDir/raw_dna/paired/F.proliferatum/A8/R/.
    cp $RawDatDir/FoxysporumN139_S2_L001_R1_001.fastq.gz $ProjectDir/raw_dna/paired/F.oxysporum_fsp_narcissi/N139/F/.
    cp $RawDatDir/FoxysporumN139_S2_L001_R2_001.fastq.gz $ProjectDir/raw_dna/paired/F.oxysporum_fsp_narcissi/N139/R/.
    cp $RawDatDir/FoxysporumPG3_S3_L001_R1_001.fastq.gz $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG3/F/.
    cp $RawDatDir/FoxysporumPG3_S3_L001_R2_001.fastq.gz $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG3/R/.
    cp $RawDatDir/FoxysporumPG18_S4_L001_R1_001.fastq.gz $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG18/F/.
    cp $RawDatDir/FoxysporumPG18_S4_L001_R2_001.fastq.gz $ProjectDir/raw_dna/paired/F.oxysporum_fsp_pisi/PG18/R/.
```

Run the assembly pipe for velvet for the strains that require assemblies



###Pisi PG18
```qsub ~/git_master/seq_tools/assemblers/velvet/assembly_pipe.sh /home/groups/harrisonlab/projects/fusarium_comp/raw_dna/paired/F.oxysporum_fsp_pisi/PG18/F/FoxysporumPG18_S4_L001_R1_001.fastq.gz /home/groups/harrisonlab/projects/fusarium_comp/raw_dna/paired/F.oxysporum_fsp_pisi/PG18/R/FoxysporumPG18_S4_L001_R2_001.fastq.gz 45 700 ~/git_master/seq_tools/assemblers/velvet/
```
###Pisi PG3
```qsub ~/git_master/seq_tools/assemblers/velvet/assembly_pipe.sh /home/groups/harrisonlab/projects/fusarium_comp/raw_dna/paired/F.oxysporum_fsp_pisi/PG3/F/FoxysporumPG3_S3_L001_R1_001.fastq.gz /home/groups/harrisonlab/projects/fusarium_comp/raw_dna/paired/F.oxysporum_fsp_pisi/PG3/R/FoxysporumPG3_S3_L001_R2_001.fastq.gz 45 700 ~/git_master/seq_tools/assemblers/velvet/
```
###Narcissi N139
```qsub ~/git_master/seq_tools/assemblers/velvet/assembly_pipe.sh /home/groups/harrisonlab/projects/fusarium_comp/raw_dna/paired/F.oxysporum_fsp_narcissi/N139/F/FoxysporumN139_S2_L001_R1_001.fastq.gz /home/groups/harrisonlab/projects/fusarium_comp/raw_dna/paired/F.oxysporum_fsp_narcissi/N139/R/FoxysporumN139_S2_L001_R2_001.fastq.gz 45 700 ~/git_master/seq_tools/assemblers/velvet/
```
