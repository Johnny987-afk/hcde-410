Exercises and assignments for HCDE410: Human Data Interaction. Everything here is a work in progress unless otherwise noted :)

## What I did

For this assignment, I looked at the Wikipedia Talk Corpus and the people who labeled comments as toxic or non-toxic. I wanted to see whether the data had problems that could affect a model trained on it. I used Python in JupyterLab to clean the worker data, make a few tables and charts, and compare the demographic information.

## What I found

One thing I noticed was that the attack and aggression worker demographic files contained the same data. Counting both files would change the demographic percentages, even though those workers should not be counted twice. I also found that 112 workers (1.94%) had no age information. For the toxicity labels, we had demographic information for 83.49% of the workers, which means there is still a group we know very little about.

I think these limitations matter because the people labeling comments may not represent everyone who uses the internet. Wikipedia comments are also different from conversations on other sites. A toxicity detector trained on these labels might not always understand jokes, slang, or how people communicate in different communities.

## Files and how to run it

- `hcde410-a2.ipynb` is my main notebook, with the code, results, and written answers.
- `wikipedia_datasets/` is the local folder containing the TSV files used in the analysis.
- I used Python 3, pandas, and matplotlib in JupyterLab.

The notebook uses the three worker demographic files (toxicity, attack, and aggression) and `toxicity_annotations.tsv` for the last section. Open the notebook and run the cells from top to bottom after putting these data files in the `wikipedia_datasets/` folder.

## Data source

[Wikipedia Talk Corpus / Wikimedia Detox](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release)

[Toxicity data on Figshare](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Toxicity/4563973)

## How I used AI

I used ChatGPT to help with parts of my Python code, debugging, and improving some of my written explanations. For example, I asked it about errors like undefined variables and why my code couldn't find toxicity_annotations.tsv.