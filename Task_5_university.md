``` sql
create table Students
(
    id             serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15) unique  not null,
    dob            date,
    date_joined    date,
    date_graduated date,
    is_graduated   boolean default false,
    is_active      boolean default true,
    gpa            real    default 0,
    grade          integer             not null,
    region_id      integer,
    group_id       integer
);


create table Departments
(
    id              serial,
    department_name varchar(100) not null,
    location_id     serial
);

create table Staffs
(
    staff_name varchar(100) not null,
    count      integer
);

create table Teachers
(
    id         serial,
    first_name varchar(100)        not null,
    last_name  varchar(100)        not null,
    username   varchar(100) unique not null,
    phone      varchar(15) unique  not null,
    subject    varchar(100)        not null
);

create table Groups
(
    group_id       serial,
    group_name     varchar(100) not null,
    group_memebers integer
);

create table Subjects
(
    subject_name         varchar(100) not null,
    weekly_lesson_counts integer
);

create table Regions
(
    region_name varchar(100) not null,
    region_id   serial
);


-- INSERT INTO

insert into departments(id, department_name, location_id)
values (01, 'Main', 0102);

insert into groups(group_id, group_name, group_memebers)
values (01, 'First group', 18);

insert into regions(region_name, region_id)
values ('Miami', 0202);

insert into staffs(staff_name, count)
values ('Director', 2),
       ('Manager', 3);

insert into students(id, first_name, last_name,
                     username, phone, dob,
                     date_joined, date_graduated, grade,
                     region_id, group_id, is_graduated,
                     is_active, gpa)
values (001, 'John', 'Steve',
        'J.Steve', '12345678', '2000-01-01',
        '2018-02-02', '2022-02-02', 87, 0202, 01,
        false, true, 2);

insert into subjects(subject_name, weekly_lesson_counts)
values ('History', 4);

insert into teachers(id, first_name, last_name, username, phone, subject)
values (01, 'Alberto', 'Brown', 'A.Brown', '123453221', 'History')
```
