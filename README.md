# apple-SEC-scanner
# Python Earnings Scanner

Built in one day, this project analyzes Apple's 10-K SEC filing (saved as `apple10k.pdf`) using Hugging Face's free Inference Providers API to extract revenue jumps, cash-flow risks, and buy-or-sell signals. It chunks the PDF for efficiency and handles errors, ideal for a quant finance demo.

## Setup Instructions

1. **Download Apple’s 10-K**  
   - Grab the PDF from [investor.apple.com/sec-filings](https://investor.apple.com/sec-filings) or [this EDGAR link](https://d18rn0p25nwr6d.cloudfront.net/CIK-0000320193/c87043b9-5d89-4717-9f49-c4f9663d0061.pdf).  
   - Save it as `apple10k.pdf` in Colab’s `/content/` directory.

2. **Install Dependencies**  
   In a Colab cell, run:
   
3. **Set Up Hugging Face API Token**   !pip install PyPDF2 huggingface_hub
- Sign up at [huggingface.co](https://huggingface.co), generate an Access Token with “Inference Providers” permissions, and set it in Colab:
  
4. **Run the Script**  
- Use the `Earnings_Scanner.ipynb` notebook in this repo.
- Upload `apple10k.pdf` to Colab’s Files tab.
- Run the notebook to get JSON output with insights like: revenue up 2% to $391B, risks from $15.8B EU tax escrow, buy signals from Services growth.

5. **GitHub** 
- This repo (`apple-sec-scanner`) contains the notebook and README, tailored for quant finance recruiters.
- Run the notebook directly in Colab via the link in `Earnings_Scanner.ipynb`.
