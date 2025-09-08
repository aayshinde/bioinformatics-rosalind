# Record of AI Assistance  

Here I describe how I made use of AI tools while working on **Beginning Bioinformatics (Part 3)**. Every program was executed and reviewed by me, and I verified outputs with small practice inputs or test datasets.  

---

## Section 1 — Setting up repo + Colab connection  
**Tool/model used:** ChatGPT (GPT-5)  
**Purpose of request:** I wanted clear steps for creating my repository, putting files into `docs/` and `notebooks/`, linking Colab to GitHub, and tagging the final submission with `week3-submission`.  
**Example of what I asked:** “Show me the exact folder paths and how to make the tag link I’ll turn in.”  
**Adjustments I made before saving:** Wrote my own line in `README.md` (with my name, ID, and course info), edited commit messages to be specific, and kept the repo public.  
**How I checked it worked:** Looked in `/notebooks/` to confirm my notebook was there, opened `docs/ai_usage.md` to see it render, and tested that the tag URL ended with `/tree/week3-submission`.  

---

## Section 2 — Practice tasks P6–P8 (input, lists, slicing)  
**Tool/model used:** ChatGPT (GPT-5)  
**Purpose of request:** Asked for tiny examples showing `input()`, list editing (insert/append/replace), and string/list slicing.  
**Example of what I asked:** “Give me quick runnable snippets I can paste into Colab for P6–P8.”  
**Adjustments I made before saving:** Changed variable names to be clearer, added comments about zero-based indexes and slice ranges, and printed values so results were obvious.  
**How I checked it worked:** Ran each snippet and compared outputs to what I expected (for example, a slice `[2:4]` gave exactly two list items).  

---

## Section 3 — Converting DNA → RNA (Rosalind #7)  
**Tool/model used:** ChatGPT (GPT-5) + Biopython (`Bio.Seq.Seq`)  
**Purpose of request:** Needed a safe way to process DNA files that might include stray spaces or text, and then convert T → U.  
**Example of what I asked:** “Help me filter the input to valid bases and then transcribe DNA into RNA.”  
**Adjustments I made before saving:** Simplified the cleaning into one line with a generator expression, and added both a plain-Python `.replace("T","U")` and Biopython approach.  
**How I checked it worked:** Compared sequence lengths (DNA vs RNA), spot-checked start and end characters, and confirmed the output was one continuous string.  

---

## Section 4 — Practice tasks P13–P15 (file reading + loops)  
**Tool/model used:** ChatGPT (GPT-5)  
**Purpose of request:** Looked for common patterns in using `read()`, `readline()`, and `readlines()`, plus how to loop through lines without printing extra blank lines.  
**Example of what I asked:** “Show me how to read files and print only specific lines neatly.”  
**Adjustments I made before saving:** Used `print(line.rstrip())` to trim newlines, added `enumerate(..., start=1)` to show line numbers, and wrote my own comments.  
**How I checked it worked:** Created a small `practice.txt`, tested loops, and confirmed the output matched (only even-numbered lines, no empty lines).  

---

## Section 5 — Word frequency dictionary (Rosalind #5)  
**Tool/model used:** ChatGPT (GPT-5)  
**Purpose of request:** Wanted both a `collections.Counter` solution and a plain dictionary method for counting words.  
**Example of what I asked:** “Show me a short solution with Counter and another one that counts words manually.”  
**Adjustments I made before saving:** Chose to keep the Counter version for clarity, printed sorted results for consistency, and added notes for readability.  
**How I checked it worked:** Tested on a short string like “red red blue” and confirmed the output matched expected counts.  

---

## Section 6 — FASTA parsing + GC% (Rosalind #9)  
**Tool/model used:** ChatGPT (GPT-5) + Biopython (`SeqIO.parse`, `SeqUtils.gc_fraction`)  
**Purpose of request:** Needed a concise script to read FASTA files, calculate GC%, and identify which record had the highest percentage.  
**Example of what I asked:** “Give me a script that prints each record’s GC% and the one with the maximum.”  
**Adjustments I made before saving:** Rounded results to 6 decimals for consistency with Rosalind outputs, and added a quick empty-sequence safeguard.  
**How I checked it worked:** Ran with a sample FASTA, manually recalculated GC% for one sequence, and confirmed the script identified the correct top ID.  

---

## Final remarks  
AI was mainly a helper for scaffolding and quick reminders. I cleaned and rewrote the final code myself, then tested each solution with sample data before committing.  
