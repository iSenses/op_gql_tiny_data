---
name: GQL_Tiny
desc: A Tiny GQL dataset means as seed for further GQL data collection and exploration.
language:
- en
dimension:
- code
sub_dimension:
- gql
website: https://github.com/iSenses/op_gql_tiny_data
github: https://github.com/iSenses/op_gql_tiny_data
paper: https://github.com/iSenses/op_gql_tiny_data
release_date: 2024-04-30
tag:
- cypher
- query
- text
download_url: https://github.com/iSenses/op_gql_tiny_data

---
## Introduction
A Tiny GQL dataset means as example for further GQL data collection and exploration.
## Meta Data
- code: cypher
- datasize: 36
- language: English
## Example
```json
{
"input_text":"Schema:
	(:Person {label: 'Person',id: string, role: string, description: string})-[:HAS_SKILL {}]->(:Skill {label:'Skill', id: string,name: string,level: string})
	(:Person {label: 'Person',id: string, role: string, description: string})-[:HAS_EDUCATION {}]->(:Education {label:'Education', id: string, degree: string, university: string, graduationDate: string, score: string, url: string})
	Question: How many people have a Ph.D. in Physics and are experts in C++?",

"output_text":"```MATCH (p:Person)-[:HAS_SKILL]->(s:Skill), (p)-[:HAS_EDUCATION]->(e:Education) WHERE toLower(s.name) CONTAINS 'c++' AND toLower(s.level) CONTAINS 'expert' AND toLower(e.degree) CONTAINS 'ph.d.' AND toLower(e.university) CONTAINS 'physics' RETURN COUNT(p)```"}
```

## Citation
