## Create a Python virtual environment
```bash
uv venv .venv
source .venv/bin/activate
```

## Install dependencies requirements for this project
```bash
pip install -r requirements.txt  -i https://pypi.tuna.tsinghua.edu.cn/simple
```

## Install dbt metricflow
```bash
pip install dbt-metricflow -i  https://pypi.tuna.tsinghua.edu.cn/simple
```

## Access duckdb by command line
```bash
duckcli jaffle_shop.duckdb
```

## Install duckdb
```bash
curl https://install.duckdb.org | sh
```

## Launch duckdb ui with:
```bash
duckdb -ui
```

## Install dbt plugin dependencies
```bash
dbt deps
```

## Build the project
```bash
dbt build
```

