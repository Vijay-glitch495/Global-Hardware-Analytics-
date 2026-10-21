# Global Hardware Analytics

**A SQL Server and MongoDB coursework/study collection for transactional data modeling and warehouse analysis.**

This repository contains operational schema scripts, warehouse transformations, analytical queries, and JSON/MongoDB exercises. It also retains course submission documents. Those documents identify an existing course/team submission; individual contributions by the repository owner are not established in this repository. Preserve that provenance and do not describe the entire collection as solely authored original work.

## Artifact map

| File | Purpose |
| --- | --- |
| `OLTP.sql`, `OLTP_Insert.sql` | Operational schema and data-loading scripts |
| `DW_CreateTables.sql` | Warehouse dimensions, sales fact, and staging tables |
| `DW_Insert.sql` | Transformations and warehouse loading |
| `DW_Queries.sql` | Sales, employee, product, and time-based analyses |
| `MONGODB_Extract.sql` | SQL Server JSON exports |
| `MongoDB_Queries.sql` | MongoDB analysis exercises; despite the extension, inspect its command syntax before running |
| `products.json`, `ProductSold.json`, `ProductStock.json` | Exported JSON artifacts |

## Concrete deliverables

The study includes dimensional modeling, SQL joins and window functions, sales aggregation, JSON export, and MongoDB aggregation. It is a code and coursework collection, not a verified production warehouse or a measured business-impact case study.

## Review workflow

```bash
git clone https://github.com/Vijay-glitch495/Global-Hardware-Analytics-.git
cd Global-Hardware-Analytics-
```

1. Inspect the schema and required database names in a disposable SQL Server database.
2. Review the operational schema before loading the supplied inserts.
3. Inspect warehouse table dependencies and transformations before executing them.
4. Validate row counts, key uniqueness, and join cardinality before interpreting query results.
5. Inspect JSON export fields and MongoDB collection names before import.

The scripts contain `DROP TABLE` statements and hard-coded coursework database names. Some definitions include trailing commas. Repair syntax and adapt paths/database names before execution; no clean database build was verified in this documentation update.

## Analytical limitations

Review each formula against its business definition. In particular, the profit-related query combines sales values with stock-based costs, so it should not be treated as a validated accounting-profit calculation. Grouping granularity and joins can also affect product rankings and totals. Descriptive inventory observations do not by themselves establish lost sales or causal demand effects.

## Attribution and license

Retain the included course/team attribution and original submission documents. See [LICENSE](LICENSE) for the repository's Mozilla Public License 2.0 terms; verify rights and attribution for included data and documents separately.
