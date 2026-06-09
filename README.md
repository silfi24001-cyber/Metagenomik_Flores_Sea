# Metagenomik_Flores_Sea
Workflow analisis metagenomik dataset Flores Sea (SRR37631993) menggunakan SRA Toolkit, Fastp, Clustal Omega, dan MEGA.
# Metagenomik_Flores_Sea

## Deskripsi

Repository ini berisi workflow analisis metagenomik menggunakan dataset Flores Sea dari NCBI SRA.

### Dataset

* BioProject: PRJNA1437532
* Run Accession: SRR37631993
* Jenis data: Shotgun Metagenomic Sequencing
* Platform: DNBSEQ
* Layout: Paired-End (2 × 150 bp)

## Workflow Analisis

### 1. Download Data

Data diunduh dari NCBI SRA menggunakan SRA Toolkit.

Perintah:

```bash
prefetch SRR37631993
```

### 2. Konversi ke FASTQ

Perintah:

```bash
fasterq-dump SRR37631993
```

Output:

* SRR37631993_1.fastq
* SRR37631993_2.fastq

### 3. Quality Control

QC dilakukan menggunakan Fastp untuk menghilangkan read berkualitas rendah dan adapter.

### 4. Analisis Taksonomi

Analisis taksonomi dilakukan menggunakan Kaiju.

### 5. Multiple Sequence Alignment

Alignment dilakukan menggunakan Clustal Omega.

### 6. Analisis Filogenetik

Pohon filogenetik dibuat menggunakan MEGA dengan metode Neighbor Joining atau Maximum Likelihood.

## Status Pekerjaan

* [x] Download dataset
* [x] Konversi SRA ke FASTQ
* [ ] Quality Control
* [ ] Alignment
* [ ] Pohon Filogenetik
* [ ] Interpretasi Hasil
