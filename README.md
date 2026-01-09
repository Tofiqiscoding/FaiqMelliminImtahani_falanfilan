-- =========================
-- IV BLOK - CAVABLAR
-- =========================

-- 1. demo_university adlı database-ni seçin
USE demo_university;

-- 2. Database-də mövcud olan bütün cədvəlləri göstərin
SHOW TABLES;

-- 3. departments cədvəlinin strukturunu göstərin
DESCRIBE departments;

-- 4. teachers cədvəlinin strukturunu göstərin
DESCRIBE teachers;

-- 5. students cədvəlinin strukturunu göstərin
DESCRIBE students;

-- 6. courses cədvəlinin strukturunu göstərin
DESCRIBE courses;

-- 7. enrollments cədvəlinin strukturunu göstərin
DESCRIBE enrollments;

-- 8. departments cədvəlində olan bütün məlumatları göstərin
SELECT * FROM departments;

-- 9. teachers cədvəlində olan bütün məlumatları göstərin
SELECT * FROM teachers;

-- 10. students cədvəlində olan bütün məlumatları göstərin
SELECT * FROM students;

-- 11. courses cədvəlində olan bütün məlumatları göstərin
SELECT * FROM courses;

-- 12. enrollments cədvəlində olan bütün məlumatları göstərin
SELECT * FROM enrollments;

-- 13. students cədvəlindən yalnız ad sahəsini göstərin
SELECT name FROM students;

-- 14. teachers cədvəlindən yalnız ad sahəsini göstərin
SELECT name FROM teachers;

-- 15. courses cədvəlindən yalnız fənn adlarını göstərin
SELECT course_name FROM courses;

-- 16. departments cədvəlindən yalnız fakültə adlarını göstərin
SELECT dept_name FROM departments;

-- 17. students cədvəlində ilk 5 məlumatı göstərin
SELECT * FROM students LIMIT 5;

-- 18. teachers cədvəlində ilk 5 məlumatı göstərin
SELECT * FROM teachers LIMIT 5;

-- 19. courses cədvəlində ilk 5 məlumatı göstərin
SELECT * FROM courses LIMIT 5;

-- 20. departments cədvəlində ilk 5 məlumatı göstərin
SELECT * FROM departments LIMIT 5;

-- 21. students cədvəlində son 5 məlumatı göstərin
SELECT * FROM students ORDER BY id DESC LIMIT 5;

-- 22. teachers cədvəlində son 5 məlumatı göstərin
SELECT * FROM teachers ORDER BY id DESC LIMIT 5;

-- 23. courses cədvəlində son 5 məlumatı göstərin
SELECT * FROM courses ORDER BY id DESC LIMIT 5;

-- 24. departments cədvəlində son 5 məlumatı göstərin
SELECT * FROM departments ORDER BY id DESC LIMIT 5;

-- 25. enrollments cədvəlində ilk 5 məlumatı göstərin
SELECT * FROM enrollments LIMIT 5;

-- 26. students cədvəlində dept_id NULL olan tələbələri göstərin
SELECT * FROM students WHERE dept_id IS NULL;

-- 27. teachers cədvəlində dept_id NULL olan müəllimləri göstərin
SELECT * FROM teachers WHERE dept_id IS NULL;

-- 28. courses cədvəlində teacher_id NULL olan kursları göstərin
SELECT * FROM courses WHERE teacher_id IS NULL;

-- 29. enrollments cədvəlində student_id NULL olan qeydləri göstərin
SELECT * FROM enrollments WHERE student_id IS NULL;

-- 30. enrollments cədvəlində course_id NULL olan qeydləri göstərin
SELECT * FROM enrollments WHERE course_id IS NULL;

-- 31. students cədvəlində dept_id 1 olan tələbələri göstərin
SELECT * FROM students WHERE dept_id = 1;

-- 32. teachers cədvəlində dept_id 1 olan müəllimləri göstərin
SELECT * FROM teachers WHERE dept_id = 1;

-- 33. courses cədvəlində teacher_id 1 olan kursları göstərin
SELECT * FROM courses WHERE teacher_id = 1;

-- 34. enrollments cədvəlində student_id 1 olan qeydləri göstərin
SELECT * FROM enrollments WHERE student_id = 1;

-- 35. enrollments cədvəlində course_id 1 olan qeydləri göstərin
SELECT * FROM enrollments WHERE course_id = 1;

-- 36. students cədvəlində adı Student1 olan tələbəni göstərin
SELECT * FROM students WHERE name = 'Student1';

-- 37. teachers cədvəlində adı Teacher1 olan müəllimi göstərin
SELECT * FROM teachers WHERE name = 'Teacher1';

-- 38. courses cədvəlində adı Course1 olan kursu göstərin
SELECT * FROM courses WHERE course_name = 'Course1';

-- 39. departments cədvəlində adı IT olan fakültəni göstərin
SELECT * FROM departments WHERE dept_name = 'IT';

-- 40. students cədvəlündə id-si 5 olan tələbəni göstərin
SELECT * FROM students WHERE id = 5;

-- 41. students cədvəlində neçə tələbə olduğunu tapın
SELECT COUNT(*) AS student_count FROM students;

-- 42. teachers cədvəlində neçə müəllim olduğunu tapın
SELECT COUNT(*) AS teacher_count FROM teachers;

-- 43. courses cədvəlində neçə kurs olduğunu tapın
SELECT COUNT(*) AS course_count FROM courses;

-- 44. departments cədvəlində neçə fakültə olduğunu tapın
SELECT COUNT(*) AS department_count FROM departments;

-- 45. enrollments cədvəlində neçə qeyd olduğunu tapın
SELECT COUNT(*) AS enrollment_count FROM enrollments;


-- =========================
-- V BLOK - CAVABLAR
-- =========================

-- 1. students cədvəlində dept_id NULL olan tələbələrin sayını tapın
SELECT COUNT(*) AS students_dept_null_count
FROM students
WHERE dept_id IS NULL;

-- 2. teachers cədvəlində dept_id NULL olan müəllimlərin sayını tapın
SELECT COUNT(*) AS teachers_dept_null_count
FROM teachers
WHERE dept_id IS NULL;

-- 3. courses cədvəlində teacher_id NULL olan kursların sayını tapın
SELECT COUNT(*) AS courses_teacher_null_count
FROM courses
WHERE teacher_id IS NULL;

-- 4. enrollments cədvəlində student_id NULL olan qeydlərin sayını tapın
SELECT COUNT(*) AS enrollments_student_null_count
FROM enrollments
WHERE student_id IS NULL;

-- 5. enrollments cədvəlində course_id NULL olan qeydlərin sayını tapın
SELECT COUNT(*) AS enrollments_course_null_count
FROM enrollments
WHERE course_id IS NULL;

-- 6. students cədvəlində dept_id dolu olan tələbələrin sayını tapın
SELECT COUNT(*) AS students_dept_notnull_count
FROM students
WHERE dept_id IS NOT NULL;

-- 7. teachers cədvəlində dept_id dolu olan müəllimlərin sayını tapın
SELECT COUNT(*) AS teachers_dept_notnull_count
FROM teachers
WHERE dept_id IS NOT NULL;

-- 8. courses cədvəlində teacher_id dolu olan kursların sayını tapın
SELECT COUNT(*) AS courses_teacher_notnull_count
FROM courses
WHERE teacher_id IS NOT NULL;

-- 9. enrollments cədvəlində tam əlaqəli qeydlərin sayını tapın
SELECT COUNT(*) AS enrollments_fully_related_count
FROM enrollments
WHERE student_id IS NOT NULL AND course_id IS NOT NULL;

-- 10. departments cədvəlində adı boş olmayan fakültələrin sayını tapın
SELECT COUNT(*) AS departments_name_notnull_count
FROM departments
WHERE dept_name IS NOT NULL;

-- 11. Tələbələri fakültə adları ilə birlikdə göstərin
SELECT s.*, d.dept_name
FROM students s
INNER JOIN departments d ON s.dept_id = d.dept_id;

-- 12. Müəllimləri fakültə adları ilə birlikdə göstərin
SELECT t.*, d.dept_name
FROM teachers t
INNER JOIN departments d ON t.dept_id = d.dept_id;

-- 13. Kursları müəllim adları ilə birlikdə göstərin
SELECT c.*, t.name
FROM courses c
INNER JOIN teachers t ON c.teacher_id = t.id;

-- 14. Qeydiyyatları tələbə adları ilə birlikdə göstərin
SELECT e.*, s.name
FROM enrollments e
INNER JOIN students s ON e.student_id = s.id;

-- 15. Qeydiyyatları kurs adları ilə birlikdə göstərin
SELECT e.*, c.course_name
FROM enrollments e
INNER JOIN courses c ON e.course_id = c.id;

-- 16. Yalnız əlaqəli olan tələbə–fakültə məlumatlarını göstərin
SELECT s.*, d.dept_name
FROM students s
INNER JOIN departments d ON s.dept_id = d.dept_id;

-- 17. Yalnız əlaqəli olan müəllim–fakültə məlumatlarını göstərin
SELECT t.*, d.dept_name
FROM teachers t
INNER JOIN departments d ON t.dept_id = d.dept_id;

-- 18. Yalnız əlaqəli olan kurs–müəllim məlumatlarını göstərin
SELECT c.*, t.name
FROM courses c
INNER JOIN teachers t ON c.teacher_id = t.id;

-- 19. Yalnız əlaqəli olan tələbə–kurs məlumatlarını göstərin
SELECT e.*, s.name, c.course_name
FROM enrollments e
INNER JOIN students s ON e.student_id = s.id
INNER JOIN courses c ON e.course_id = c.id;

-- 20. Əlaqəsiz (NULL) tələbələri göstərin
SELECT s.*, d.dept_name
FROM students s
LEFT JOIN departments d ON s.dept_id = d.dept_id
WHERE d.dept_id IS NULL;

-- 21. Əlaqəsiz (NULL) müəllimləri göstərin
SELECT t.*, d.dept_name
FROM teachers t
LEFT JOIN departments d ON t.dept_id = d.dept_id
WHERE d.dept_id IS NULL;

-- 22. Əlaqəsiz (NULL) kursları göstərin
SELECT c.*, t.name
FROM courses c
LEFT JOIN teachers t ON c.teacher_id = t.id
WHERE t.id IS NULL;

-- 23. Əlaqəsiz (NULL) qeydiyyatları göstərin
SELECT e.*, s.name, c.course_name
FROM enrollments e
LEFT JOIN students s ON e.student_id = s.id
LEFT JOIN courses c ON e.course_id = c.id
WHERE s.id IS NULL OR c.id IS NULL;

-- 24. Yalnız ilk 5 əlaqəli tələbəni göstərin
SELECT s.*, d.dept_name
FROM students s
INNER JOIN departments d ON s.dept_id = d.dept_id
LIMIT 5;

-- 25. Yalnız ilk 5 əlaqəli kursu göstərin
SELECT c.*, t.name
FROM courses c
INNER JOIN teachers t ON c.teacher_id = t.id
LIMIT 5;

-- 26. students cədvəlini ada görə sıralayın
SELECT * FROM students ORDER BY name;

-- 27. teachers cədvəlini ada görə sıralayın
SELECT * FROM teachers ORDER BY name;

-- 28. courses cədvəlini ada görə sıralayın
SELECT * FROM courses ORDER BY course_name;

-- 29. departments cədvəlini ada görə sıralayın
SELECT * FROM departments ORDER BY dept_name;

-- 30. students cədvəlində NULL dəyərləri olan sahələri göstərin
SELECT * FROM students WHERE dept_id IS NULL;

-- 31. teachers cədvəlində NULL dəyərləri olan sahələri göstərin
SELECT * FROM teachers WHERE dept_id IS NULL;

-- 32. courses cədvəlində NULL dəyərləri olan sahələri göstərin
SELECT * FROM courses WHERE teacher_id IS NULL;

-- 33. enrollments cədvəlində NULL dəyərləri olan sahələri göstərin
SELECT * FROM enrollments
WHERE student_id IS NULL OR course_id IS NULL;

-- 34. Əlaqəli 5 tələbəni göstərin
SELECT s.*, d.dept_name
FROM students s
INNER JOIN departments d ON s.dept_id = d.dept_id
LIMIT 5;

-- 35. Əlaqəli 5 müəllimi göstərin
SELECT t.*, d.dept_name
FROM teachers t
INNER JOIN departments d ON t.dept_id = d.dept_id
LIMIT 5;

-- 36. Əlaqəli 5 kursu göstərin
SELECT c.*, t.name
FROM courses c
INNER JOIN teachers t ON c.teacher_id = t.id
LIMIT 5;

-- 37. Əlaqəli 5 qeydiyyatı göstərin
SELECT e.*, s.name, c.course_name
FROM enrollments e
INNER JOIN students s ON e.student_id = s.id
INNER JOIN courses c ON e.course_id = c.id
LIMIT 5;

-- 38. Əlaqəsiz tələbələrin sayını tapın
SELECT COUNT(*) AS unrelated_students_count
FROM students s
LEFT JOIN departments d ON s.dept_id = d.dept_id
WHERE d.dept_id IS NULL;

-- 39. Əlaqəsiz müəllimlərin sayını tapın
SELECT COUNT(*) AS unrelated_teachers_count
FROM teachers t
LEFT JOIN departments d ON t.dept_id = d.dept_id
WHERE d.dept_id IS NULL;

-- 40. Əlaqəsiz kursların sayını tapın
SELECT COUNT(*) AS unrelated_courses_count
FROM courses c
LEFT JOIN teachers t ON c.teacher_id = t.id
WHERE t.id IS NULL;

-- 41. Əlaqəsiz qeydiyyatların sayını tapın
SELECT COUNT(*) AS unrelated_enrollments_count
FROM enrollments e
LEFT JOIN students s ON e.student_id = s.id
LEFT JOIN courses c ON e.course_id = c.id
WHERE s.id IS NULL OR c.id IS NULL;

-- 42. students cədvəlində məlumat olub-olmadığını yoxlayın
SELECT CASE
         WHEN COUNT(*) > 0 THEN 'Məlumat var'
         ELSE 'Məlumat yoxdur'
       END AS students_status
FROM students;

-- 43. teachers cədvəlində məlumat olub-olmadığını yoxlayın
SELECT CASE
         WHEN COUNT(*) > 0 THEN 'Məlumat var'
         ELSE 'Məlumat yoxdur'
       END AS teachers_status
FROM teachers;

-- 44. courses cədvəlində məlumat olub-olmadığını yoxlayın
SELECT CASE
         WHEN COUNT(*) > 0 THEN 'Məlumat var'
         ELSE 'Məlumat yoxdur'
       END AS courses_status
FROM courses;

-- 45. enrollments cədvəlində məlumat olub-olmadığını yoxlayın
SELECT CASE
         WHEN COUNT(*) > 0 THEN 'Məlumat var'
         ELSE 'Məlumat yoxdur'
       END AS enrollments_status
FROM enrollments;
