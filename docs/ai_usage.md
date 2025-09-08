**AI Usage Log

Notes on how I incorporated AI support while completing Beginning Bioinformatics (Part 3). I ran and reviewed all final code myself and confirmed outputs using test cases and small datasets.

Entry 1 — Repo setup and GitHub/Colab workflow

Tool/model & version: ChatGPT (GPT-5)
What I asked for: Clear, step-by-step directions for creating my GitHub repo, adding the correct docs/ and notebooks/ folders, saving my Colab notebook to notebooks/Bioinformatics_Module03.ipynb, and tagging the submission as week3-submission.
Snippet of prompt(s): “Explain exactly how to connect Colab with GitHub and show me the tag link I need to turn in.”
What I changed before committing: Wrote my own line in README.md (name + UTA ID + course/section), adjusted commit messages so they describe what I did, and kept the repo open.
How I verified: Checked that the notebook renders in /notebooks/, that docs/ai_usage.md displays properly, and that the tag URL shows /tree/week3-submission.

Entry 2 — Practice problems P6–P8 (input, lists, slicing)

Tool/model & version: ChatGPT (GPT-5)
What I asked for: Small code fragments to demonstrate input handling, list modifications (insert/append/replace), and string/list slicing.
Snippet of prompt(s): “Give me short examples of list slicing and inserting elements that I can run directly in Colab.”
What I changed before committing: Renamed some variables for clarity, added my own explanatory comments (like slice behavior and index positions), and printed outputs so results are easy to follow.
How I verified: Ran each snippet and confirmed expected results (e.g., a slice [2:4] produced exactly the two items I expected).

Entry 3 — Rosalind DNA→RNA problem (#7)

Tool/model & version: ChatGPT (GPT-5) + Biopython (Bio.Seq.Seq)
What I asked for: A notebook cell that converts DNA to RNA, even if the input file has stray text or extra characters.
Snippet of prompt(s): “Show me a safe way to filter sequence letters and then replace T with U.”
What I changed before committing: Simplified the filter step to a one-liner using a generator, and kept both a plain Python .replace("T","U") and a Biopython method side by side.
How I verified: Checked that the lengths of DNA and RNA strings match, reviewed first/last chunks manually, and ensured output is continuous with no breaks or spaces.

Entry 4 — Practice problems P13–P15 (file I/O + loops)

Tool/model & version: ChatGPT (GPT-5)
What I asked for: Patterns for reading files using read(), readline(), readlines(), plus clean looping without printing extra blank lines.
Snippet of prompt(s): “Show me examples of reading files and printing only certain lines neatly.”
What I changed before committing: Switched to print(line.rstrip()) to avoid empty lines, used enumerate(..., start=1) for counting, and added clarifying comments.
How I verified: Tested with a small practice file and confirmed correct outputs (e.g., only even-numbered lines appeared, no unexpected spacing).

Entry 5 — Word counts with dictionaries (Rosalind #5)

Tool/model & version: ChatGPT (GPT-5)
What I asked for: Both a collections.Counter solution and a basic dictionary loop for word counting.
Snippet of prompt(s): “Give me two different versions of word count, one short with Counter and one that builds counts manually.”
What I changed before committing: Kept the Counter version for readability, ensured results are sorted before printing so they’re consistent, and added comments.
How I verified: Tried with a short sample string (like “apple apple banana apple”) and checked that counts matched expectations.

Entry 6 — FASTA parsing + GC% (Rosalind #9)

Tool/model & version: ChatGPT (GPT-5) + Biopython (SeqIO.parse, SeqUtils.gc_fraction)
What I asked for: A simple routine to read FASTA sequences, compute GC%, and identify the record with the highest GC content.
Snippet of prompt(s): “Give me concise code to parse FASTA, print GC for each ID, and report the top one.”
What I changed before committing: Rounded outputs to 6 decimal places to match Rosalind formatting and added a quick check in case of empty sequences.
How I verified: Ran on the sample FASTA, manually checked GC for one sequence, and confirmed the reported highest GC ID matches.

Closing note

I used AI as a helper for structure, reminders, and small code patterns. The final code, formatting, and tests were done by me. I double-checked every solution against sample inputs before committing.**
