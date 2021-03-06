---
layout: tutorial_hands_on
topic_name: additional-analyses
tutorial_name: reopening-apollo-with-annotations
---

> ### Agenda
>>
> 1. Import Apollo data into Galaxy
> 2. Rearrange the Genome
> 3. Re-upload the Organism into Apollo
>
{: .agenda}

# Import Apollo data into Galaxy

Import Apollo data into Galaxy using the [Retrieve Data](https://cpt.tamu.edu/galaxy-pub/root?tool_id=edu.tamu.cpt2.webapollo.export) tool. You will get three files from this step (FASTA, GFF3, Json).  

# Rearrange the Genome

Then, use the [Genome Editor](https://cpt.tamu.edu/galaxy-pub/root?tool_id=edu.tamu.cpt.gff3.genome_editor) tool in Galaxy to edit the genome appropriately: delete extra sequence, add missing sequence, or re-open at the appropriate position.  

Select as input the GFF3 and FASTA data retrieved from Apollo, and click on “Insert sequence component selections” to concatenate them together. You need to fill in a new ID name for the edited genome (like Phage.v2). 


![](../../images/reopening-apollo-with-annotations-screenshots/1-editor-tool.png)


> ### {% icon tip %} Please note...
> If you add missing sequences, new gene calls may be needed at the newly added region.  You will lose any annotation that is split by reopening.
{: .tip}

# Re-upload Organism into Apollo

After the organism is edited/reopened, import and run the **“Upload Previously Annotated Sequence to Apollo (v2020.XX)” workflow** in [Published workflows](https://cpt.tamu.edu/galaxy-pub/workflows/list_published) to upload and view the new Apollo record.  

> ### {% icon tip %} Note that…
> This creates a new organism, which you must give a new name (like Phage.v2) . Check the features in the re-opened genome to ensure accuracy.  You may need to re-run structural and functional workflow for the re-opened genome to add annotation tracks to the new Apollo record, and to fix gene calls and annotations, especially for the edited regions.
{: .tip}
