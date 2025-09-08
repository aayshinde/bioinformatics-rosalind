# AI Use Log  

Quick notes on where I used AI while completing **Beginning Bioinformatics (Part 3)**. I wrote and ran all final code myself and double-checked outputs with small test files and examples.  

---

## Entry 1 — GitHub + Colab wiring  
**Tool/model & version:** ChatGPT (GPT-5)  
**What I asked for:** Step-by-step help to set up my repo, create `docs/` and `notebooks/`, save my Colab notebook to `notebooks/Bioinformatics_Module03.ipynb`, and make a `week3-submission` tag.  
**Snippet of prompt(s):** “I’m new to GitHub and Colab — show me exactly how to connect them and generate the tag link for submission.”  
**What I changed before committing:** Added my own line in `README.md` (Name + UTA ID + section), wrote clearer commit messages, and kept the repo public.  
**How I verified correctness:** Confirmed that the notebook appears in `/notebooks/`, that `docs/ai_usage.md` renders properly, and that the tag link ends in `/tree/week3-submission`.  

---

## Entry 2 — P6–P8 (input, lists, slicing)  
**Tool/model & version:** ChatGPT (GPT-5)  
**What I asked for:** Small examples for using `input()`, list operations (`append`, `insert`, `replace`), and slicing strings/lists.  
**Snippet of prompt(s):** “Show me short Colab-ready examples for P6–P8 problems.”  
**What I changed before committing:** Renamed variables to be clearer, added comments on 0-based indexing and slicing behavior, and printed outputs to make results obvious.  
**How I verified correctness:** Ran each cell and checked outputs matched expectations (e.g., `my_list[2:4]` returned the correct slice).  

---

## Entry 3 — Rosalind #7 (DNA → RNA)  
**Tool/model & version:** ChatGPT (GPT-5) + Biopython (`Bio.Seq.Seq`)  
**What I asked for:** A safe way to transcribe DNA to RNA, even when the file had stray text or blank lines.  
**Snippet of prompt(s):** “Filter the input to valid A/C/G/T only, then replace T with U.”  
**What I changed before committing:** Simplified the cleaning step with a generator expression and included both a plain Python `.replace("T","U")` and a Biopython solution.  
**How I verified correctness:** Checked DNA and RNA lengths, spot-checked beginning and end of sequences, and confirmed the RNA output is one continuous string.  

---

## Entry 4 — P13–P15 (file I/O + loops)  
**Tool/model & version:** ChatGPT (GPT-5)  
**What I asked for:** Examples of reading files (`read()`, `readline()`, `readlines()`) and looping cleanly without printing blank lines.  
**Snippet of prompt(s):** “Show file-reading patterns and how to only print certain lines neatly.”  
**What I changed before committing:** Used `print(line.rstrip())` in loops, added `enumerate(..., start=1)` for line numbering, and explained why in comments.  
**How I verified correctness:** Tested on a sample text file and confirmed that only even lines printed, without extra spacing.  

---

## Entry 5 — Word count with dictionaries (Rosalind #5)  
**Tool/model & version:** ChatGPT (GPT-5)  
**What I asked for:** Both a `Counter` solution and a pure dictionary approach for counting words.  
**Snippet of prompt(s):** “Give me a short word count using `Counter` and another version that updates counts manually.”  
**What I changed before committing:** Kept the Counter version for readability, sorted the results before printing, and added comments for clarity.  
**How I verified correctness:** Ran with a short test string (e.g., “apple apple banana”) and confirmed output counts matched.  

---

## Entry 6 — FASTA parsing + GC% (Rosalind #9)  
**Tool/model & version:** ChatGPT (GPT-5) + Biopython (`SeqIO.parse`, `SeqUtils.gc_fraction`)  
**What I asked for:** A concise script to parse FASTA files, compute GC content, and report the sequence with the highest GC%.  
**Snippet of prompt(s):** “Make a simple parser that prints GC% for each ID and identifies the maximum.”  
**What I changed before committing:** Rounded to 6 decimals to match Rosalind format and added a check for empty sequences.  
**How I verified correctness:** Ran on a sample FASTA, confirmed GC calculations by hand for one sequence, and validated that the reported max matched.  

---

## Closing note  
I relied on AI for quick scaffolding and reminders, but I rewrote, cleaned, and verified all final code myself. Each solution was tested with small datasets before committing.  
