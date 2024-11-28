```sql
SQL > select fst_name,lst_name,job 
2	from users 
3	where user_id = 001;

FST_NAME       LST_NAME         JOB
-------------- -------------- --------------
Nicolò         Vitelli        Data Engineer

SQL > select t.tech_name product
2	from users u
3		inner join user_tech ut on u.user_id = ut.user_id
4		inner join technologies t on ut.tech_id = t.tech_id 
5	where u.user_id = 001;

PRODUCT    
-----------------------
Oracle SQL
Oracle PL/SQL
Oracle Data Integrator
Oracle Stream Analytics
Oracle GoldenGate
Informatica PowerCenter

SQL > select c.contact_name || ' ' || c.contact_url contacts
2	from users u
3		inner join user_cont uc on u.user_id = uc.user_id
4		inner join contacts c on uc.contact_id = c.contact_id 
5	where u.user_id = 001;

CONTACTS         
---------------------------------------------------------
Linkedin   https://www.linkedin.com/in/nvitelli/
GitHub     https://github.com/nicolovitelli/nicolovitelli
