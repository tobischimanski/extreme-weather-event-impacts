# Extreme Weather Event Impacts: Data, Models and Code

This is the GitHub repository for the paper "[What Firms Actually Lose (and Gain) from Extreme Weather Event Impacts](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6035794)". It includes the datasets and the code to create it.

## Data
The simplest form of the project is the 13,277 firm-event impacts. This is created analysing over 1.7 million filings (3.5 billion paragraphs) of all publicly listed firms in the US. We analyse filing types: event-based Form 8-K, quarterly reported Form 10-Q, and annually reported Form 10-K. We upload all paragraphs that are at least containing a mention of a extrme weather event / physical risk in a more fine-grained dataset.

### Event-Impact Data
This is the final data including the 13,277 firm-event impacts (**name: event_impact_data.csv**). It has the following structure:
- event_id: ID of the event in the NOAA billion-dollar dataset
- cik: unique company identifier [If this combination is present, then there was a firm-event impact]
- asset, economic_flows, none: classification dimensions of the impact channel classifier; shows whether at least one document indicated an asset impact (asset==1), a pure economic flow impact, i.e. at least one document was only addressing an impact through economic flows and NOT through assets as well (economic_flows==1), or none if at least one document mentioned a none impact (neither asset, nor economic flows; none==1)
- neutral, negative, positive, reimbursement: classification dimensions of the impact dimensionality classifier; shows whether at least one document indicated a neutral, negative, or positive impact, or a reimbursement 
- name: event name according to NOAA
- event_type: disaster event type according to NOAA
- begin_date: event begin date according to NOAA
- cpi_adjusted_cost: CPI-adjusted cost of the event according to NOAA

As a complementary dataset, we also upload the NOAA extreme weather event dataset (**name: NOAA_events_2005-2024_with_summary.csv**), [obtained here](https://www.ncei.noaa.gov/access/billions/):
- Name: event name according to NOAA
- Disaster: disaster event type according to NOAA
- Begin Date: event begin date according to NOAA
- End Date: event end date according to NOAA
- CPI-Adjusted Cost: CPI-adjusted cost of the event according to NOAA
- Unadjusted Cost: non-adjusted cost of the event according to NOAA
- Deaths: deaths caused by the event according to NOAA
- Event Duration: event duration according to NOAA
- Event ID: ID of the event in the NOAA billion-dollar dataset
- Summary: event description / summary provided by NOAA

### File-based Data
See [HuggingFace repository](https://huggingface.co/extreme-weather-impacts).

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


