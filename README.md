# Al-Khwarizmi-3B — Chat

Live chat notebook for **[Al-Khwarizmi-3B](https://huggingface.co/mzoelfakar/Al-Khwarizmi-3B)**, an AI math tutor named after Muhammad al-Khwarizmi, the 9th-century mathematician whose name is the direct origin of the word "algorithm". The model is a fine-tuned version of `HuggingFaceTB/SmolLM3-3B-Base` using the `GSM8K` dataset.

This repo exists to let anyone try the model online via Colab, with no local setup required.

## Run it online

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mzoelfakar/Al-Khwarizmi-3B/blob/main/Al-Khwarizmi-3B.ipynb)

Click the badge above, then run the cell — it loads the model and starts an interactive chat loop directly in the Colab output.

## About the model

Full training details, benchmarks, and usage snippets are on the model card: **[mzoelfakar/Al-Khwarizmi-3B](https://huggingface.co/mzoelfakar/Al-Khwarizmi-3B)**.

## Note on raw output formatting

Because the model was fine-tuned on GSM8K (including the `socratic` reasoning style), raw generations may contain training artifacts not meant for direct display:

- `<<...>>` — calculator-style intermediate annotations
- `**` — separator between a sub-question and its calculation in Socratic-style reasoning (not Markdown bold)
- `#### <answer>` — marker preceding the final numeric answer
- `*` — used as a multiplication sign (e.g. `8*9`); if two or more appear in the same response, Markdown may pair them as emphasis delimiters, causing the text between them to render in italics with the asterisks hidden

This notebook already handles these cases before rendering. If you adapt the display logic elsewhere, you'll want to account for them too.

## License

apache-2.0

## Credits

Fine-tuned by [Mohamed Zoelfakar](https://www.linkedin.com/in/mzoelfakar/), as part of Hugging Face's [smol-course](https://huggingface.co/learn/smol-course/).
