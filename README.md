# study_process_database
Учебная база данных для SQL Server, тема Учебный процесс в вузе 

1) Загружаем MS SQL Server (SQL Server Management Studio 2019 were used here)
2) Запускаем .sql скрипт, база локально развернется на вашем ПК

**Диаграмма БД**

![image](https://user-images.githubusercontent.com/89765480/147278099-dae491db-20de-4048-97a0-25ef682f3dfe.png)


Also included BookShopDB .sql script


```psql
-- change varchar constraint to int 
ALTER TABLE client DROP CONSTRAINT client_pkey CASCADE;
ALTER TABLE client ALTER COLUMN id TYPE integer USING (id::integer);
ALTER TABLE client ADD CONSTRAINT client_pkey PRIMARY KEY (id);
ALTER TABLE client RENAME id TO clientId;
```
