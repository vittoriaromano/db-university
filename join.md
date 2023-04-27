1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
- SELECT * 
FROM `students` 
JOIN `degrees` ON `degrees`.`id` = `students`.`degree_id` 
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze 
- SELECT * 
FROM `departments` 
JOIN `degrees` ON `departments`.`id` = `degrees`.`id` 
WHERE `degrees`.`level` = 'magistrale' 
AND `departments`.`name` = 'Dipartimento di Neuroscienze';

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
- SELECT * 
FROM `courses` 
JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`teacher_id` 
JOIN `teachers` ON `teachers`.`id` = `course_teacher`.`course_id` 
WHERE `teachers`.`id` = '44';

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome 
- SELECT `students`.* 
FROM `students` 
JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id` 
JOIN `departments` ON `departments`.`id` = `degrees`.`department_id` 
ORDER BY `students`.`surname`, `students`.`name`;

5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
- ? 

6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)
- 
7. BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per
superare ciascuno dei suoi esami
- 
