1. Contare quanti iscritti ci sono stati ogni anno

SELECT COUNT(`id`) AS `num_studenti`, YEAR(`enrolment_date`) AS `anno_di_iscrizione`
FROM `students`
GROUP BY `anno_di_iscrizione`;

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT COUNT(`id`) AS `num_insegnanti`, `teachers`.`office_address` AS `ufficio`
FROM `teachers`
GROUP BY `ufficio`;

3. Calcolare la media dei voti di ogni appello d'esame

SELECT AVG(`vote`), `exam_student`.`exam_id`
FROM `exam_student`
GROUP BY `exam_student`.`exam_id`;

4. Contare quanti corsi di laurea ci sono per ogni dipartimento

SELECT COUNT(`degrees`.`id`) AS `corsi_di_laurea`, `degrees`.`department_id`
FROM `degrees`
GROUP BY `degrees`.`department_id`;