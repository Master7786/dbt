SELECT count(1)  FROM `data-terraform-338612.dbt_dataset.fact_trips` 
where date(pickup_datetime) between '2019-01-01' and '2020-12-31';


select count(1)  FROM `data-terraform-338612.dbt_dataset.fact_fhv_trips` ;

select count(1) from `trips_data_all.fhv_external`;

select date_trunc(pickup_datetime, month), count(tripid) from `dbt_dataset.fact_fhv_trips` group by 
date_trunc(pickup_datetime, month) order by count(tripid) desc;