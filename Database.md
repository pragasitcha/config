## PostGres 

max connection problem 

select current connections , superuser connections , max connections 

select  * from
(select count(*) used from pg_stat_activity) q1,
(select setting::int res_for_super from pg_settings where name=$$superuser_reserved_connections$$) q2,
(select setting::int max_conn from pg_settings where name=$$max_connections$$) q3;

edit maxconnections 
/var/lib/pgsql/11/data/postgresql.conf

restart systemctl restart postgresql-11
status systemctl status postgresql-11
