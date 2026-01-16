# Extreme Weather Event Impacts: Data, Models and Code

This is the GitHub repository for the paper "[What Firms Actually Lose (and Gain) from Extreme Weather Event Impacts](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6035794)". It includes the datasets and the code to create it.

## Data
The simplest form of the project is the 13,277 firm-event impacts. This is created analysing over 1.7 million filings (3.5 billion paragraphs) of all publicly listed firms in the US. We analyse filing types: event-based Form 8-K, quarterly reported Form 10-Q, and annually reported Form 10-K. We upload all paragraphs that are at least containing a mention of a extrme weather event / physical risk in a more fine-grained dataset.

### Event-Impact Data

### File-based Data

## Models
We upload all models, and training data on [HuggingFace in this repository](https://huggingface.co/extreme-weather-impacts). Model usage is described in the corresponding model pages.

## Repository under construction
The repository is currently being constructed. If you have any questions, please reach out to tobias.schimanski@df.uzh.ch.

## Paper
If you make use of the data, please cite [the paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6035794):

```shell
@article{schimanski2026extremeweatherimpacts,
  title        = {What Firms Actually Lose (and Gain) from Extreme Weather Event Impacts},
  author       = {Schimanski, Tobias and Gostlow, Glen and Toetzke, Malte and Leippold, Markus},
  url          = {https://ssrn.com/abstract=6035794},
  doi          = {10.2139/ssrn.6035794}
}
```


