SQL link:

https://sqlfiddle.com/mysql/online-compiler?id=0f960b20-854e-45a6-a47c-ec1a4aaa694c


CREATE TABLE Books (
    book_id INT PRIMARY KEY,
    title VARCHAR(100),
    author VARCHAR(100)
);

CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(100)
);

CREATE TABLE IssueRecords (
    issue_id INT PRIMARY KEY,
    book_id INT,
    student_id INT,
    issue_status VARCHAR(20),
    FOREIGN KEY (book_id) REFERENCES Books(book_id),
    FOREIGN KEY (student_id) REFERENCES Students(student_id)
);

SELECT * FROM Books;
SELECT * FROM IssueRecords;

