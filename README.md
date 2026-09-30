# Australian Education Services Analysis

An exploratory analysis of education and care services across Australian states and territories: service supply, NQS quality ratings, recorded public-transport proximity, estimated demand and approved capacity.

## View the project

- **Interactive website:** https://yunmf19.github.io/australia-education-services-analysis/
- **QA state/service-type comparison:** https://yunmf19.github.io/australia-education-services-analysis/charts/qa-below-nqs.html
- **All static figures:** https://yunmf19.github.io/australia-education-services-analysis/report.html

Use the website URL, rather than a local `C:` path or GitHub source-file URL, as a PowerPoint hyperlink. Charts support hover; relevant charts also provide region and service-type filters. The website bundles Plotly locally.

## Contents

- `individual_assignment_option_a.ipynb`: latest analysis code, with saved outputs removed from the public notebook.
- `docs/`: ready-to-publish interactive charts and latest static figures.
- `requirements.txt`: core versions used in the working environment.
- `DATA.md`: required local inputs and interpretation notes.

The publication package excludes raw service records, course presentations, backups, temporary files and older notebooks. It is a source-and-results package; it does not redistribute all source data.

## Run locally

1. Use Python 3.11 or later (the working environment used Python 3.14).
2. Create a virtual environment and install dependencies: `python -m pip install -r requirements.txt`.
3. Put the input files listed in `DATA.md` beside the notebook, preserving their filenames.
4. Run `python -m pip install jupyterlab`, then `jupyter lab` from this repository directory.
5. Open the notebook and run cells from the beginning in order.

The notebook displays charts in place. It contains no automatic HTML/image/CSV export cells and no statistical hypothesis-test sections. Published pages are a snapshot of its latest saved figure outputs.

To preview the website without any input data: `python -m http.server 8000 --directory docs`, then open http://localhost:8000 .

## Interpretation

- Below NQS combines **Working Towards NQS** and **Significant Improvement Required**. Denominators include recognized current ratings separately for each quality area.
- National rates pool service records; they are not unweighted averages of state percentages.
- The proximity measure uses the smaller valid recorded bus/train distance for each service and compares it with the pooled national median nearest distance (currently 2.32 km). The full-precision threshold is shared by all states; the median is less sensitive to extreme distances than the mean. The station list is not established as a complete public-transport inventory.
- Urban/rural comparisons use the notebook's SOS classification; unmatched categories are grouped as Rural under the stated analytical rule.
- Capacity boxplots use observed positive places for the selected end-of-2024 Centre-Based Care cohort. Other capacity views retain their documented imputation rules.
- The birth-cohort proxy is not a current resident-population estimate. These descriptive comparisons do not establish causality.

No license for third-party source data is granted by this repository. Obtain input data from the relevant provider and follow its terms.
