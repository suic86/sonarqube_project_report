Sonarqube project report
===

Generates a csv or an xlsx file reflecting sonarqube's project dashboard.

Usage
---

```shell
usage: report.py [-h] [-t {csv,xlsx}] report_filename [project_tag]

positional arguments:
  report_filename       Output report file name.
  project_tag           Project tag.

optional arguments:
  -h, --help            show this help message and exit
  -t {csv,xlsx}, --report-type {csv,xlsx}
```

Queries all projects available. Filter using `tagname`(s) if you just need a limited view.
Generates csv report at `filename` location - overwrites existing files.

Installation
- 

+ Install dependencies: \
`pip install -r requirements.txt`

+ Configure environment variables:\
`SONARQUBE_API_BASE` base path to api - e.g. https://sonarqube.example.com/api/ \
`SONARQUBE_API_USERTOKEN` user token used for basic authentication. See https://docs.sonarqube.org/latest/user-guide/user-token/ for details.

How to read the report
-

Every line represents a project. Columns show the project metrics using the keys explained here: https://docs.sonarqube.org/latest/user-guide/metric-definitions/ \
Character ranges A to F are transformed to numeric values (A = 1, B = 2, ...).
