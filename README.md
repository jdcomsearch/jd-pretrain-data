# jd-pretrain-data

jd-pretrain-data is an open-source dataset for user intent detection and embedding retrieval which is collected from search system of JD.com. Due to business information confidentiality, we only show **encoded id** of search query, item title and product category id. The project contains 5 tab-separated values (TSV) files, each of which has the following headers:

* pretrain_data.tsv: item title \t product category
* finetune_data_uid.tsv: query \t aggregated product categories
* finetune_data_er.tsv: query \t item title
* eval_overall.tsv: query \t aggregated product categories \t aggregated items' title
* eval_tail.tsv: same as eval_overall.tsv

User intent detection and embedding retrieval tasks share the same pre-train and evaluation datasets, but use different finetune datasets. Concretely,  **finetune_data_uid.tsv** is the finetune dataset for user intent detection task while **finetune_data_er.tsv** is for embedding retrieval task.  **eval_overall.tsv** and **eval_tail.tsv** stand for evaluation dataset on overall and long-tail query respectively.

For more details, feel free to check out our CIKM 2022 paper: https://arxiv.org/pdf/2208.06150.pdf
