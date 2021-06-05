# MYSQL_JKUAT_DTB
-- phpMyAdmin SQL Dump
-- version 5.1.0
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Jun 05, 2021  18:53 AM
-- Server version: 10.4.19-MariaDB
-- PHP Version: 8.0.6
SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";
/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */; --
-- Database: `jomo kenyatta [jkuat]` --
-- --------------------------------------------------------
--
-- Table structure for table `campus` --CREATE TABLE `campus` (
`campus_id` int(200) NOT NULL, `campus_name` varchar(200) NOT NULL, `campus_location` varchar(200) NOT NULL, `campus_address` varchar(200) NOT NULL, `campus_population` int(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4; --
-- Dumping data for table `campus` --
INSERT INTO `campus` (`campus_id`, `campus_name`, `campus_location`, `campus_address`, `campus_population`) VALUES
(1, 'Main Campus', 'Juja ,Kiambu', 'Juja 20465', 377576), (2, 'Karen', 'Nairobi', 'Nairobi 37495', 7465774), (3, 'Kitale', 'Trans Nzoia', 'Kitale 2393', 377576), (4, 'Kilifi', 'Kilifi ', 'Kilifi 287', 7465774); -- --------------------------------------------------------
--
-- Table structure for table `colleges` --CREATE TABLE `colleges` (
`college_id` int(30) NOT NULL, `college_name` varchar(30) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;--
-- Dumping data for table `colleges` --
INSERT INTO `colleges` (`college_id`, `college_name`) VALUES
(1, 'COETEC'), (2, 'COHES'), (3, 'COPAS'), (4, 'COHRED'); -- --------------------------------------------------------
--
-- Table structure for table `course` --CREATE TABLE `course` (
`course_id` int(30) NOT NULL, `course_name` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4; --
-- Dumping data for table `course` --
INSERT INTO `course` (`course_id`, `course_name`) VALUES
(1, 'Mathematics and computer science'), (2, 'Computer science'),(3, 'Civil Engineering'), (4, 'Teaching'), (5, 'Financial Engineering'), (6, 'Bachelor in information and technology'), (7, 'Information technology'), (8, 'Business and commerce'); -- --------------------------------------------------------
--
-- Table structure for table `departments` --CREATE TABLE `departments` (
`department_id` int(30) NOT NULL, `depatment_name` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4; --
-- Dumping data for table `departments` --
INSERT INTO `departments` (`department_id`, `depatment_name`) VALUES
(2, 'Pure and applied mathematics '), (3, 'Human resource'), (4, 'Mechanical Engineering'), (5, 'Counseling'), (6, 'Actuarial science'), (7, 'Drugs and Vaccination'),(8, 'Pure Finance'), (9, 'Pure mathematics'); -- --------------------------------------------------------
--
-- Table structure for table `lectures` --CREATE TABLE `lectures` (
`lecturer_id` int(20) NOT NULL, `lecturer_name` varchar(100) NOT NULL, `address` varchar(30) NOT NULL, `phone_number` int(10) NOT NULL, `gender` varchar(2) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4; --
-- Dumping data for table `lectures` --
INSERT INTO `lectures` (`lecturer_id`, `lecturer_name`, `address`, `phone_number`, `gender`) VALUES
(25647, 'sam mbure', ' Juja 4945', 756858474, 'M'), (848595, 'prince katie', ' Kiambu 8484', 753436936, 'M'), (3748576, 'sylvia muthoni', ' Nairobi 8484', 76474363, 'F'), (27736454, 'janice jane', ' Kitale 4945', 757374654, 'F'); -- ----------------------------------------------------------
-- Table structure for table `schools` --CREATE TABLE `schools` (
`school_id` int(11) NOT NULL, `school_name` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4; --
-- Dumping data for table `schools` --
INSERT INTO `schools` (`school_id`, `school_name`) VALUES
(1, 'Mathematical science '), (2, 'Humanity'), (3, 'Engineering'), (4, 'Nursing'), (5, 'Business and accounting'), (6, 'Architecture'), (7, 'Physical Sciences'), (8, 'Pharmarcy'); -- ----------------------------------------------------
--
-- Table structure for table `students` --CREATE TABLE `students` (
`students_id` int(200) NOT NULL, `student_name` varchar(200) NOT NULL, `address` int(30) NOT NULL, `dataBirth` timestamp(6) NOT NULL DEFAULT current_timestamp(6) ON UPDATE current_timestamp(6), `year_of_study` int(10) NOT NULL, `gander` varchar(2) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4; --
-- Dumping data for table `students` --
INSERT INTO `students` (`students_id`, `student_name`, `address`, `dataBirth`, `year_of_study`, `gander`)
VALUES
(1, 'Clinton njogu', 8912, '2021-06-03 08:36:08.000000', 2, 'M'), (2, 'vincent okoth', 8484, '2011-06-13 08:36:08.000000', 1, 'M'), (3, 'seth Rollins', 3949, '2012-06-20 08:38:33.000000', 3, 'M'), (4, 'Dyline Acheing', 3884, '2014-06-04 08:39:51.000000', 1, 'F'), (5, 'Purity nyaguthii', 38849, '2013-06-12 08:39:51.000000', 2, 'F'); --
-- Indexes for dumped tables
--
--
-- Indexes for table `campus` --ALTER TABLE `campus`ADD PRIMARY KEY (`campus_id`); --
-- Indexes for table `colleges` --ALTER TABLE `colleges` ADD PRIMARY KEY (`college_id`); --
-- Indexes for table `course` --ALTER TABLE `course` ADD PRIMARY KEY (`course_id`); --
-- Indexes for table `departments` --ALTER TABLE `departments` ADD PRIMARY KEY (`department_id`); --
-- Indexes for table `lectures` --ALTER TABLE `lectures` ADD PRIMARY KEY (`lecturer_id`); --
-- Indexes for table `schools` --ALTER TABLE `schools` ADD PRIMARY KEY (`school_id`); --
-- Indexes for table `students` --ALTER TABLE `students` ADD PRIMARY KEY (`students_id`); --
-- AUTO_INCREMENT for dumped tables
--
--
-- AUTO_INCREMENT for table `campus` --ALTER TABLE `campus` MODIFY `campus_id` int(200) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=5; --
-- AUTO_INCREMENT for table `colleges` --ALTER TABLE `colleges` MODIFY `college_id` int(30) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=5; --
-- AUTO_INCREMENT for table `course` --ALTER TABLE `course`MODIFY `course_id` int(30) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=9; --
-- AUTO_INCREMENT for table `departments` --ALTER TABLE `departments` MODIFY `department_id` int(30) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=10; --
-- AUTO_INCREMENT for table `schools` --ALTER TABLE `schools` MODIFY `school_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=9; --
-- AUTO_INCREMENT for table `students` --ALTER TABLE `students` MODIFY `students_id` int(200) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;
COMMIT;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION
