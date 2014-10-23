fastAQ
======

fastAQ is a fast and super lightweight package for working with FASTA/FASTQ sequences. 


<b>Download</b> : 

        git clone https://github.com/Jverma/fastAQ
    or  https://pypi.python.org/pypi/fastaq

<b>Install</b> :

              pip install fastaq 
          or  python setup.py develop
                

<b>Dependencies</b> : None

<b>Documentation</b> : to be added.

<b>Command line Usage:</b>

    git clone https://github.com/Jverma/fastAQ
    
Notation:
    
    $location = location of the fastAQ folder on your computer.
    $fasta = location/fastAQ/fastAQ/commandLineTools/fasta.py
    $fastq = location/fastAQ/fastAQ/commandLineTools/fasta.py
    $fastq2fasta = location/fastAQ/fastAQ/commandLineTools/fastq2fasta.py


Conver a FASTQ file into a FASTA file

    python fastq2fasta input_file.fastq 
  
List containing the names/headers of all the sequences in the FASTA/Q file.
    
    python fasta input_file.fasta -seqNames 
    python fastq input_file.fastq -seqNames
    
Sequences corresponding to the names/headers in a text file. 
  
    python fasta input_file.fasta -seq names_file.txt
    python fastq input_file.fastq -seq names_file.txt
    
Qualities of the sequences corresponding to the names/headers in a text file.

    python fastq input_file.fastq -qual names_file.txt

Trim sequences corresponding to the names in a text file according to the intervals in another file. 
  
    python fasta input_file.fasta -trim names_file.txt interval_file.txt
    python fastq input_file.fastq -trim names_file.txt interval_file.txt
    
Mask sequences corresponding to the names in a text file according to the intervals in another file.

    python fasta input_file.fasta -mask names_file.txt interval_file.txt
    python fastq input_file.fastq -mask names_file.txt interval_file.txt
    
Reverse Complement sequences corresponding to the names in a text file. 
  
    python fasta input_file.fasta -reverseComplement names_file.txt
    python fastq input_file.fastq -reverseComplement names_file.txt
    
Reverse Complement all the sequences in the given file. 

    python fasta input_file.fasta -reverseComplementAll
    python fastq input_file.fastq -reverseComplementAll
    
Trim all the sequences in the given file (remove intervalStart bases from left and intervalEnd bases from right). 

    python fasta input_file.fasta -trimAll -intervalStart=1 -intervalEnd=5
    python fastq input_file.fastq -trimAll -intervalStart=1 -intervalEnd=5
    
Mask all the sequences in the given file (masks intervalStart bases from left and intervalEnd bases from right). 

    python fasta input_file.fasta -maskAll -intervalStart=1 -intervalEnd=5
    python fastq input_file.fastq -maskAll -intervalStart=1 -intervalEnd=5
    
    
Trim FASTQ sequences in the file by removing low quality bases (quality > qualityCutOff).

    python fastq input_file.fastq -trimLowQuality names_file.txt -qualityCutOff=30
    
Trim FASTQ sequences according to the Mott's algorithm (choose limitValue)

    python fastq input_file.fastq -mottTrim names_file.txt -limitValue=0.65
    
Trim all FASTQ sequences by removing low quality bases. 

    python fastq input_file.fastq -trimAlllowQuality -qualityCutOff=30
    
Trim all FASTQ sequences by Mott's algorithm. 

    python fastq input_file.fastq -mottTrimAll -limitValue=0.65

    
    
    

 
