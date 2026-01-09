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

-- 40. students cədvəlində id-si 5 olan tələbəni göstərin
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
