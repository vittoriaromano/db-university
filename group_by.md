1. Contare quanti iscritti ci sono stati ogni anno
- SELECT YEAR(`enrolment_date`) AS `enrolment_year`, 
 COUNT(`id`)
 AS `enroled_students`
 FROM `students`
 GROUP BY YEAR(`enrolment_date`);

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
- SELECT `office_address` AS `adress`, 
COUNT(`id`) 
FROM `teachers` 
GROUP BY `office_address`;

3. Calcolare la media dei voti di ogni appello d'esame
- SELECT `exam_id` AS `session`, AVG(`vote`) AS `vote_avarage` 
FROM `exam_student` 
GROUP BY `exam_id`;

4. Contare quanti corsi di laurea ci sono per ogni dipartimento
- SELECT `department_id` AS `department`, 
COUNT(`id`)  AS `course_number`
FROM `degrees` 
GROUP BY `department_id`;
