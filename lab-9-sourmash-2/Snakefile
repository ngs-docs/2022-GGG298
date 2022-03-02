SAMPLES=[1,2,3,4,5]

rule all:
    input:
        "all.cmp.hist.png"

rule download:
    output:
        expand("{sample}.fa.gz", sample=SAMPLES)
    shell:"""    
wget https://osf.io/t5bu6/download -O 1.fa.gz
wget https://osf.io/ztqx3/download -O 2.fa.gz
wget https://osf.io/w4ber/download -O 3.fa.gz
wget https://osf.io/dnyzp/download -O 4.fa.gz
wget https://osf.io/ajvqk/download -O 5.fa.gz
"""

rule compute:
    input:
        "{sample}.fa.gz",
    output:
        "{sample}.fa.gz.sig",
    shell:"""
sourmash compute -k 31 {input}
"""

rule compare:
    input:
        expand("{sample}.fa.gz.sig", sample=SAMPLES)
    output:
        cmp="all.cmp",
        text="all.cmp.labels.txt"
    shell:
        "sourmash compare {input} -o {output.cmp}"

rule plot:
    input: 
        cmp="all.cmp",
        text="all.cmp.labels.txt"
    output:
        "all.cmp.hist.png",
        "all.cmp.dendro.png",
        "all.cmp.matrix.png"
    shell:
        "sourmash plot --labels {input.cmp}"
