# jdsearch-22

jdsearch-22 is an open-source dataset for user intent detection and embedding retrieval which is collected in search platform of JD.com. Due to confidential business information protection, we only show **encoded id** of search query, item title and product category id. The project contains 5 tsv format files. The headers are shown as below:

* pretrain_data.tsv: item title \t product category
* finetune_data_uid.tsv: query \t aggregated product categories
* finetune_data_er.tsv: query \t item title
* eval_overall.tsv: query \t aggregated product categories \t aggregated items' title
* eval_tail.tsv: same as eval_overall.tsv

User intent detection and embedding retrieval tasks share with same pretrain and evaluation dataset, but different finetune datasets. For evaluation, "overall" and "tail" stands for evaluation on overall and long-tail query, respectively.

For more details, feel free to check out our CIKM 2022 paper: https://arxiv.org/pdf/2208.06150.pdf