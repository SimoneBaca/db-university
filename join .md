1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT students.*, degrees.name AS degrees_name
FROM students
JOIN degrees
ON degree_id = degrees.id
WHERE degrees.name = "Corso di Laurea in Economia";

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

SELECT degrees.*, departments.name
FROM degrees
JOIN departments
ON department_id = departments.id
WHERE departments.name = "Dipartimento di Neuroscienze"
AND level = "Magistrale";

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

SELECT courses.name, courses.description, courses.period
FROM course_teacher
JOIN courses
ON course_id = courses.id
WHERE teacher_id = 44
ORDER BY courses.period;

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il
relativo dipartimento, in ordine alfabetico per cognome e nome



5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti


6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)



7. BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per
superare ciascuno dei suoi esami