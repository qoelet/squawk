---
id: prefer-identity
title: prefer-identity
---

## problem

Serial types make permissions and schema management difficult. Identity columns are standard SQL and have more features and better usability.

## solution

Instead of:

```sql
create table app.users
(
    id  bigserial
)
```

Use:

```sql
create table app.users
(
    id  bigint generated by default as identity primary key
)
```

## links

- https://wiki.postgresql.org/wiki/Don%27t_Do_This#Don.27t_use_serial
- https://www.enterprisedb.com/blog/postgresql-10-identity-columns-explained
