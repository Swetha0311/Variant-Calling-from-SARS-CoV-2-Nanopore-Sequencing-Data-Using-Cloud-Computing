# Variant-Calling-from-SARS-CoV-2-Nanopore-Sequencing-Data-Using-Cloud-Computing

# Overview

This project explores cloud-based variant calling using SARS-CoV-2 Nanopore sequencing data. By leveraging Amazon EMR and Apache Spark, we aim to enhance computational efficiency, scalability, and reproducibility compared to traditional HPC-based workflows.

# Problem Statement

Variant calling from SARS-CoV-2 Nanopore sequencing data is computationally intensive, requiring efficient read alignment, mutation detection, and filtering. Traditional HPC systems struggle with scalability and cost, whereas cloud computing offers a dynamic, cost-effective solution.

# Data Description

Source: Public dataset PRJNA750736 (15 SARS-CoV-2 Nanopore sequencing samples).

Storage: Uploaded to AWS S3 for easy access and processing.

Size: ~30MB per sample.

# Methodology

1. Preprocessing (HPC-based)

Quality assessment using FASTQC

Read trimming with Trim Galore

2. Cloud Data Management

Upload preprocessed data & reference genome to AWS S3

Configured Amazon EMR cluster with Apache Spark

3. Variant Calling Workflow

Minimap2 for sequence alignment

Samtools for file conversion (SAM → BAM)

LoFreq for SNP & Indel detection

Execution through the AWS EMR cluster

4. Performance Comparison

Cloud-based variant calling completed in 1 hour

Traditional HPC processing took ~2 hours

# Dependencies & Tools Used

AWS Services: S3, EC2, IAM, EMR

Bioinformatics Tools: Minimap2, Samtools, LoFreq, FASTQC, Trim Galore

Big Data Processing: Apache Spark

