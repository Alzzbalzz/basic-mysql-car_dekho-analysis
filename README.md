use cars;
select * from car_dekho;
-- to get the total count of total records --
select count(*) from car_dekho;
-- How many available cars in 2023 --
select count(*) from car_dekho where year = 2023;
-- how many cars available in 2020,2021,2022--
select count(*) from car_dekho where year in (2022, 2021,2020) group by year;
-- total of cars by year, no extra details--
select year, count(*) as total_count from car_dekho group by year;
-- how many diesel car in 2020--
select count(*) from car_dekho where year= 2020 and fuel= 'Diesel';
-- all the fuel cars comes by year--
select year, count(*) as total_count from car_dekho where fuel='Petrol'group by year;
select year, count(*) as total_count from car_dekho where fuel='Diesel'group by year;
select year, count(*) as total_count from car_dekho where fuel='CNG'group by year;
-- which year had more than 100 cars--
select year, count(*)as total_count from car_dekho group by year having total_count>100;
select year, count(*)as total_count from car_dekho group by year having total_count<50;
-- all car details count between 2015-2023, complete list--
select count(*) from car_dekho where year between 2015 and 2023;
-- all car details between 2015-2023, complete list--
select * from car_dekho where year between 2015 and 2023;
