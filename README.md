# Usage Guide
Dataset for library misuse paper.

## 1 - Repo Structure


File / Folder | Description
 --- | --- 
misuse_cases_in_1018_conntracts.xlsx | lists misuse cases found in `./1018_real_world_contracts`
misuse_cases_in_audited_contracts(card_sorting).xlsx | lists card information of library misuse in `./audit_reports.zip`, and card sorting result
vulnerable_contracts_propagation_analysis.xlsx | lists the address and deploy time of real-world Ethereum contracts which used vulnerable libraries related to P1, P2, and P3
library_popularity_analysis.xlsx | lists Ethereum library sorted by usage number
audit_reports.zip | lists 5 pdf files containing the audit reports of the corresponding 5 audit companies
1018_real_world_contracts | contains 1018 randomly selected contracts from Ethereum


## 2 - Usage Guide of each file / folder

### 1: `misuse_cases_in_1018_conntracts.xlsx`
This excel file contains library misuse cases found in 1018 real-world contracts (Section 5). You can check different types `{PATTERN}` of  misuse cases according to the contract file path `./1018_real_world_contracts/{CONTRACT_NAME}` and the locations (specific lines) `{MISUSE_LOCATION}`.

**Data Field:**

Field | Description
 --- | ---
CONTRACT_NAME | the contract file name, and the file can be find in `./1018_real_world_contracts/{CONTRACT_NAME}`. The name format is: `{deploy_time}`_`{contract_address}`.sol
MISUSE LOCATION | location (specific line) of misuse cases in the contract, multiple locations are split by the commas, such as `200,221,245` 
MISUSE_NUMBER | the misuse case number in the contract 
PATTERN | the misuse pattern of the listed cases


### 2: `misuse_cases_in_audited_contracts(card_sorting).xlsx`

This excel file contains cards information and the card sorting result we mentioned in Misuse Pattern Confirmation (Section 3.4). You can locate `./audit_report.zip/{COMPANY}.pdf` and specific page `{LOCATION}` to check each cards.

**Data Field:**

Field | Description
 --- | ---
ID | card ID
INFO | card info: the vulnerability description
CODE | card info: the vulnerability code example
COMPANY | card info: the audit company who found this vulnerability
LOCATION | card info: the vulnerability location in the corresponding audit company's report file (`./audit_report.zip/ {COMPANY}.pdf`)
Person 1 | card sorting: volunteer_1's result 
Person 2 | card sorting: volunteer_2's result 
COMMENTS | card sorting: discussion for a consistent result
COMBINED RESULT | card sorting: consistent result 


### 3: `vulnerable_contracts_propagation_analysis.xlsx`
This excel file lists contracts which contains vulnerable libraries from 468,744 Ethereum contracts since 2015 (Section 5.5). You can check the  vulnerable libraries by search `{address}` from `etherscan.io`

Field | Description
 --- | ---
Time & Contract Address | the deploy time and the address of the contracts, the format is {deploy-year-month}/{address}.sol 
Pattern | the misuse pattern 

### 4: `library_popularity_analysis.xlsx`

This excel file lists popular Ethereum libraries sorted by their usage number in real-world contracts that we mentioned in the Library Popularity Analysis (Section 3.2). 

Field | Description
 --- | ---
Time & Contract Address | the deploy time and the address of the contracts, the format is `{deploy_year-deploy_month}/{contract_address}.sol` 
Pattern | the misuse pattern 

### 5: `audit_reports.zip`
This zip file lists 5 pdf files containing the audit reports of the corresponding 5 audit companies. You can locate `./audit_report.zip/{COMPANY}.pdf` and specific page `{LOCATION}` to check each cards according to the `misuse_cases_in_audited_contracts(card_sorting).xlsx`.

### 6: `1018_real_world_contracts`
This folder contains 1018 randomly selected contracts from Ethereum. The file name format is `{deploy_year_month}_{contract_address}.sol`. You can check different types `{PATTERN}` of  misuse cases according to the contract file path `./1018_real_world_contracts/{CONTRACT_NAME}` and the locations (specific lines) `{MISUSE_LOCATION}`according to the `misuse_cases_in_1018_conntracts.xlsx`.
