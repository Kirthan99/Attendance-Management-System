

# Attendance Management System using Face Recognition

## Overview

The **Attendance Management System using Face Recognition** is a Python-based application, which automates the attendance tracking process using facial recognition technology. This system utilizes libraries such as **OpenCV** for face capturing and recognition purposes, making it secure, accurate, and efficient in managing attendance. It is applicable in educational institutions, workplaces, or any other place that needs to track attendance.

## Technologies Used

This project uses the following technologies and libraries:

1. **OpenCV**: Real-time image processing and video stream capture for the detection and recognition of faces.
2. **NumPy**: Mathematical operations on images and manipulation of arrays/matrices within facial recognition algorithms.
3. **Pandas**: Handling and manipulating attendance data stored in tabular formats, such as CSV or MySQL database.
4. **Pillow**: Image processing tasks, including loading, converting, and saving images in various formats.
5. **Matplotlib**: Plotting attendance data by creating charts and graphs to analyze trends
6. **Dlib**: Toolkit for facial recognition and landmark detection in facial images
7. **Tkinter**: GUI interaction with the application
8. **Jupyter Notebook**: Prototyping and testing the code with an interactive approach
9. **VS Code**: An Integrated Development Environment for the development and debugging of the code.
10. **MySQL Database**: The attendance records, user details such as name, and enrollment number, and the log of attendance are safely stored in this database.

## Features

- **Face Detection & Recognition**: A webcam captures real-time images and a trained machine learning model identifies and recognizes faces in those images to record attendance only by the authenticated individuals.
- **Automatic Attendance Tracking**: The system automatically tracks attendance by matching the recognized faces with records in the database.
- **Live Updations**: Attendance records are updated live, including the live tracking of attendance record along with historical records.
- **Attendance Reports**: It also gives a graphical report and insights over the attendance patterns using Matplotlib.
- **Database Support**: Saves the attendance record and the information of users securely in MySQL for permanent data management.
- **User-Friendly GUI**: The simple and user-friendly GUI is built by using Tkinter so as to be easy to operate.
- **Enrollment Feature**: The feature of enrolling face with **name** and **enrollment number** for later automatic attendance marking by the system.

## Advantages

- **Automation**: Manual entry of attendance is removed. This eliminates the scope of human error and saves time.
- **Security & Accuracy**: Only authorized individuals' attendance can be logged. This reduces proxy attendance.
- **Real-Time Updates**: Attendance is marked in real time and gives instant data processing.
- **Data Insights**: It gives insights into attendance trends over time, which helps in monitoring user attendance.
- **Cost-Effective**: It reduces the need for traditional paper-based attendance systems and manual entry.
- **Scalability**: It can be adapted to different environments like schools, universities, offices, and large organizations.

## How It Works

The system works in the following steps:

### 1. Take Images for Enrollment
- The enrollment number and name are asked for by the user during the enrollment process.
   - After the user inputs his details, the system captures multiple images from various angles using the webcam to create a dataset for face recognition. The captured images along with the name and enrollment number are saved in the database for future reference.

### 2. **Train the Model**
- Once enough images are taken, the system processes these images to extract **facial embeddings**, which are unique numerical representations of the user's face.
   - These embeddings, along with the user's **name** and **enrollment number**, are stored in the **MySQL database**. The system then trains a face recognition model based on this data to be used later for automatic attendance marking.

### 3. **Automatic Attendance**
- After the model is trained, the system starts capturing real-time video from a webcam. Once a registered user enters the frame, the system detects and identifies his face.
   - If there is a match, the system automatically records the **name**, **enrollment number**, **date**, and **time** of attendance in the database.

### 4. **Manual Attendance**
- If the system fails to recognize a user's face because of factors such as poor lighting or obstruction, then the system can be marked **manually**.
 - A list will appear in the GUI from where the user will select their **name** and **enrollment number** for marking their attendance manually.

---

## Installation and Setup

To install and set up the system on your local machine, please follow these steps:

### Prerequisites

- Python 3.x
- MySQL Database Server
- Jupyter Notebook (for testing and prototyping)
- Visual Studio Code (IDE for development)

### Step 1: Clone the Repository


```bash
git clone https://github.com/Kirthan99/Attendance-Management-System-using-Face-Recognition-main.git
cd Attendance-Management-System-using-Face-Recognition-main
```


### Step 2: Install Necessary Libraries

Use `pip` to install all necessary Python libraries:


```bash
pip install -r requirements.txt
```

This will download libraries such as:

-opencv-python
numpy
pandas
pillow
matplotlib
dlib
tkinter
mysql-connector-python 

### Step 3: Configure MySQL Database

1. **Create a Database**: Start by creating a new MySQL database, such as `attendance_system`.

```sql
CREATE DATABASE attendance_system;
```

2. **Create the Attendance Table**: Now set up the table to hold all the attendance records.

```sql
CREATE TABLE attendance (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    enrollment_number VARCHAR(20),
    date DATE,
    time TIME
);
```

3. **Update Database Configuration**: Update the connection details in the `db_connector.py` file with your MySQL database credentials.

### Step 4: Run the Application

1. Open the `attendance_system.py` script or run the Jupyter notebook to start the system.
2. The GUI window will appear, where you can enroll faces, register users, and mark attendance automatically.

## Real-Time Use Cases

1. **Educational Institutions**: Schools and universities can automate student attendance, ensuring accurate records and reducing the workload on teachers.
2. **Corporate Offices**: Organizations can track employee attendance more efficiently, particularly in large companies with many employees.
3. **Event Management**: The system can be used for event or conference participant registration and attendance tracking.
4. **Access Control**: Face recognition can be used in secure areas for access control. Access is granted to only authorized personnel based on face recognition.

## Challenges and Problems Solved

1. **Accuracy**: Attendance is recorded for the right person with face recognition technology, eliminating proxy attendance.
2. **Real-Time Processing**: Attendance is marked instantly, giving real-time information without delay.
3. **Efficient Data Management**: MySQL database integration provides secure and reliable storage for attendance records.
4. **User-Friendly Interface**: Tkinter-based GUI ensures easy interaction with the system, reducing the learning curve for users.

## Future Improvements

- **Improved Face Recognition**: Improved accuracy under various lighting conditions and different facial expressions.
- **Mobile Application**: The system to be developed as a mobile version of the system so that the users can mark their attendance from any location.
- **Multi-Camera Support**: Supports the use of multiple cameras for better coverage and recognition in large environments.

## License

Licensed under the MIT License. See [LICENSE](LICENSE) for more details.

---

 
