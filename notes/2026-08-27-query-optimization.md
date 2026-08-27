# 2026-08-27: Query optimization notes

- Use `EXPLAIN ANALYZE` before changing queries.
- Prefer predicate pushdown in Spark; filter early.
- Avoid `SELECT *` in production jobs.
- When joining large tables, broadcast the smaller side if < 10MB (or tune `spark.sql.autoBroadcastJoinThreshold`).
- Test on a sample before running full refresh.