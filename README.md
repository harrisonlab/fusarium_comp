#fusarium_comp


Run the build_dir.pl script to make a directory structure
Usage: build_dir.pl <projectname.csv>
where the csv is a comma delimited file with the following:
DNA,PE,fusarium_comp,various

/home/harrir/git_master/seq_tools/directory_structure/build_dir.pl /home/harrir/projects/git_projects/fusarium_comp/fusarium_comp.csv 

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
