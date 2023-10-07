**Speedway-Grand-Prix-2015-2023**

As a huge fan of the speedway and data analysis I wanted to **present this exciting sport to a wider audience by building a dashboard**. 

The designed dashboard allows users to discover statistics such as:
* Who has **the most number of champion titles**?
* Who has **the most number of SGP wins**?
* What **country has the most SGP wins**?
* What **country has the highest number of athletes**?
* Which **countries organize the SGP round**?
* Which **countries have their representative in SGP**?

The dashboard provides answers for other interesting facts from Speedway World. On the last page called **Highlights**, you can read the **major insights of the Speedway Grand Prix**.

**The process of designing and building the dashboard contains steps**:

1. Data scrapping from [gurustats.pl](https://gurustats.pl/) and [https://en.wikipedia.org/](https://en.wikipedia.org/wiki/Main_Page)
2. Building relationships between imported tables in Power BI
3. Designing a layout of the dashboard
4. Creating measures
5. Building charts
6. Writing descriptions and conclusions for the highlights page

**Technology**:
* Python - pandas, numpy, selenium, datetime
* Power BI

**Project Challenges**:
* Column names from gurustats data contained special characters - **Solution**: used regex to clean data
* Scraped data didn't allow the creation of star model and relationships - **Solution**: during scrapping data was divided into separate tables and indexes were created by concatenating columns e.g AthleteID = ROK + Zawodnik
* More advanced metrics have not been available directly from created tables - **Solution**: A virtual table has been created with SUMMARIZE(), ADDCOLUMNS() and CALCULATE() functions
* Showing data labels on the map is not directly accessible in Power BI - **Solution**: added additional columns containing longitude and latitude data for each country,
  and as a location measure Rounds Per Country has been used to show the country and number of organized SGP rounds e.g. Polska: 3

![data_model](https://github.com/PJarr/Speedway-Grand-Prix-2015-2023/assets/123145712/c0e7001c-c138-408c-a9f0-f71d6aa3283a)
![overview](https://github.com/PJarr/Speedway-Grand-Prix-2015-2023/assets/123145712/604b4ff1-f558-4bf8-96ae-07e4860bd390)
![zawodnicy](https://github.com/PJarr/Speedway-Grand-Prix-2015-2023/assets/123145712/3b64d812-cadc-46e8-a2fd-46317d4d7844)
![reprezentacje](https://github.com/PJarr/Speedway-Grand-Prix-2015-2023/assets/123145712/62c6d68b-e5d1-42da-82fa-7b65c59cff4a)
![highlights](https://github.com/PJarr/Speedway-Grand-Prix-2015-2023/assets/123145712/800e7c44-71c8-4ee5-80f6-fe3efee07b09)

**Selected measures**:
<br />
<br />
![Średnia Liczba Zawodników na Reprezentację](https://github.com/PJarr/Speedway-Grand-Prix-2015-2023/assets/123145712/643ad601-d910-474c-a547-64621bd9f3b7)
![Państwo_z_najwieksza_liczba_rund](https://github.com/PJarr/Speedway-Grand-Prix-2015-2023/assets/123145712/76faead0-d778-45e8-beb7-b2ae7a098367)


