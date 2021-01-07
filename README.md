## Pipe Processing Language

Piped Processing Language (PPL), powered by Open Distro for Elasticsearch, enables Open Distro for Elasticsearch users with exploration and discovery of, and finding search patterns in data stored in Elasticsearch, using a set of commands delimited by pipes (|). These are essentially read-only requests to process data and return results.

Currently, Open Distro for Elasticsearch users can query data using either Query DSL or SQL. Query DSL is powerful and fast. However, it has a steep learning curve, and was not designed as a human interface to easily create ad hoc queries and explore user data. SQL allows users to extract and analyze data in Elasticsearch in a declarative manner. Open Distro for Elasticsearch now makes its search and query engine robust by introducing Piped Processing Language (PPL). It enables users to extract insights from Elasticsearch with a sequence of commands delimited by pipes (|). It supports a comprehensive set of commands including search, where, fields, rename, dedup, sort, eval, head, top and rare, and functions, operators and expressions. Even new users who have recently adopted Open Distro for Elasticsearch, can be productive day one, if they are familiar with the pipe (|) syntax. It enables developers, DevOps engineers, support engineers, site reliability engineers (SREs), and IT managers to effectively discover and explore log, monitoring and observability data stored in Open Distro for Elasticsearch.

We expand the capabilities of our Workbench, a comprehensive and integrated visual query tool currently supporting only SQL, to run on-demand PPL commands, and view and save results as text and JSON. We also add a new interactive standalone command line tool, the PPL CLI, to run on-demand PPL commands, and view and save results as text and JSON.

The query start with search command and then flowing a set of command delimited by pipe (|). | for example, the following query retrieve firstname and lastname from accounts if age large than 18.

```
source=accounts
  | where age > 18
  | fields firstname, lastname
```

## [Request for Comments (RFC)](https://github.com/opendistro-for-elasticsearch/sql/blob/develop/docs/experiment/ppl/RFC_%20Pipe%20Processing%20Language.pdf)
Please add your feature requests here [New Requests](https://github.com/opendistro-for-elasticsearch/sql/issues) and view project progress [here](https://github.com/orgs/opendistro-for-elasticsearch/projects).

## License

This project is licensed under the Apache-2.0 License.

