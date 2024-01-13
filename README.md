Display the total amount of patients for each province. Order by descending.

SELECT pr.province_name, count(patient_id)
FROM patients p 
join province_names pr on p.province_id=pr.province_id
group by p.province_id
order by count(patient_id) DESC;
