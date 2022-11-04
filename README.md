# evaluate_dbt

steps to evaluate [dbt](https://www.getdbt.com/)

- create virtual environment with python3 and activate it
```
python -m venv .venv
source .venv/bin/activate
```
- install requirements (based on https://docs.getdbt.com/docs/get-started/pip-install)
```
python -m pip install --upgrade pip
python -m pip install -r requirements/base.txt
```
- verify install
```
dbt --version
```
- create sample project (will ask for connections details. Those are then stored in your ~/.dbt/profiles.yml) <p>
inspired from https://www.startdataengineering.com/post/dbt-data-build-tool-tutorial/
```
dbt init <project_name>
```
cd <project_name>
- check connection to db
```
dbt debug
```
- implement the changes in the db
```
dbt run
```
- run tests in the db
```
dbt test
```
- generate documentation
```
dbt docs generate
dbt docs serve
```

References:
- https://www.reddit.com/r/dataengineering/comments/stzuur/dbt_vs_spark/
- https://www.youtube.com/watch?v=8FZZivIfJVo

More advanced example:
- https://github.com/josephmachado/simple_dbt_project
