1. Az adott témának megfelelő SQL adatbázis megtervezése (legalább 5 tábla, minimum 3NF-ben legyen)

    Logikai modell


    Fizikai modell
```js

CREATE TABLE [dbo].[Oktatok](
	[Oktaz] [nvarchar](255) PRIMARY KEY,
	[Nev] [nvarchar](255) NOT NUll, 
	[Email] [nvarchar](255) NOT NULL,
	[Kezd Cim] [nvarchar](255) NOT NUll, 
	[Rendszam] [nvarchar](7) NOT NULL,
	[Oraber] [int]
 )

```








```js

CREATE TABLE [dbo].[Tanulok](
	[Tanaz] [nvarchar](255) PRIMARY KEY,
	[Nev] [nvarchar](255) NOT NUll, 
	[Email] [nvarchar](255) NOT NULL,
	[Telefonszam] [int] NOT NUll, 
	[Lakcim] [nvarchar](255) NOT NULL,
	[Oaz] [nvarchar](255) NOT NULL
 )

```







```js

CREATE TABLE [dbo].[Autok](
	[Rendszam] [nvarchar](9) PRIMARY KEY,
	[Tipus] [nvarchar](255) NOT NUll, 
	[Valto] [nvarchar](255) NOT NULL,
	[Vasarlas Datuma] [DATE] NOT NUll, 
	[Megtett út] [INT] NOT NULL
 )
 
```










```js

CREATE TABLE [dbo].[Elso_Segely](
  	[KurzusAz] [int] PRIMARY KEy,
	[Terem] [nvarchar](255) NOT NULL,
	[Tanaz] [nvarchar](255) NOT NUll, 
	[Idopont] [date],
	[Kurzus Vizsga?] [nvarchar](4) NOT NUll, 
	[Kurzus Dij] [int] NOT NULL
 )

```





```js

CREATE TABLE [dbo].[Vizsga](
	[Vizsga idopont] [date] PRIMARY Key,
	[Tan Az.] [nvarchar](255) NOT NUll, 
	[Vizsga tipus] [nvarchar](255) NOT NULL,
	[Valto] [nvarchar](255) NOT NUll, 
	[Utvonal] [int] NOT NULL,
	[Oktaz] [nvarchar](255) NOT NULL
 )

```


    Az adatbázis feltöltése tesztadatokkal vagy adatok importálása


    Hasznos lekérdezések elkészítése, amelyek kihasználják a tanultakat (5-6 db)


    Választható témák: személyi kölcsönök nyilvántartása, telefon előfizetések nyilvántartása, háziorvosi rendelő adatbázisa, labdarúgó bajnokság mérkőzéseinek nyilvántartása, autósiskola adatbázisa, többfordulós tehetségkutató verseny adatbázisa, fodrászüzlet adatbázisa, autókereskedő adatbázisa
    Beadandó: a modellek, az adatbázis leírása + az adatbázis és a lekérdezések kódja (.sql) GitHub repository-ba feltöltve (elég a repository linkjét megadni) + readme fájlban a csoporttagok neve