# **Automated Attendance Face Recognition**

## **Project Overview**
The **Automated Attendance Face Recognition** system is designed to automate the process of attendance tracking using facial recognition technology. This project leverages computer vision to identify individuals and mark their attendance efficiently. The system can be used in educational institutions, workplaces, or any environment where attendance monitoring is necessary.

## **Features**
- **Face Recognition**: Detects and recognizes faces from images or live video feeds.
- **Attendance Logging**: Automatically marks attendance for recognized faces and stores records.
- **Real-time Processing**: Captures and processes video streams in real time for fast and accurate attendance.
- **Secure and Scalable**: Ensures data security and can be easily integrated into larger systems.
- **Detailed Reports**: Generates attendance reports for individuals or groups over specific time periods.

## **Tech Stack**
- **Python**: Core programming language used.
- **OpenCV**: For image and video processing.
- **dlib/face_recognition library**: For face detection and recognition.
- **Flask/Django (Optional)**: For creating a web-based interface.
- **SQLite/MySQL**: For storing attendance records.

## **Getting Started**

### **Prerequisites**
To run this project locally, you will need the following:
- **Python 3.x** installed
- **pip** for package management
- Webcam or camera for live video feed

### **Installation**

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/automated-attendance-face-recognition.git
   cd automated-attendance-face-recognition
   ```

2. **Create a Virtual Environment (Optional but recommended)**
   ```bash
   python3 -m venv env
   source env/bin/activate  # For Linux/Mac
   env\Scripts\activate     # For Windows
   ```

3. **Install Dependencies**
   Install the required Python libraries by running:
   ```bash
   pip install -r requirements.txt
   ```

4. **Prepare Dataset**
   - Add images of individuals in the `/dataset` directory. The folder structure should be as follows:
     ```
     dataset/
        person1/
            img1.jpg
            img2.jpg
        person2/
            img1.jpg
            img2.jpg
     ```

5. **Run the Application**
   ```bash
   python main.py
   ```

6. **Access Web Interface (Optional)**
   If you’ve implemented a web interface, access the app at:
   ```
   http://localhost:5000
   ```

## **Usage**

- Launch the script to start face recognition.
- The system will automatically detect and log attendance for registered faces.
- You can view and export attendance reports from the system.

## **Branches**

- `main`: Contains the stable version of the project.
- `development`: For ongoing development and new features.
- `feature-branch`: Specific feature implementation.

## **Contributing**

We welcome contributions to enhance the project. To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit and push your changes (`git push origin feature-branch`).
5. Open a Pull Request.

## How to become a contributor and submit your own code

![Screen Shot 2022-08-30 at 7 27 04 PM](https://user-images.githubusercontent.com/42785357/187579207-9924eb32-da31-47bb-99f9-d8bf1aa238ad.png)

### Typical Pull Request Workflow -

**1. New PR**

- As a contributor, you submit a New PR on GitHub.
- We inspect every incoming PR and add certain labels to the PR such as `size:`,
  `comp:` etc.  At this stage we check if the PR is valid and meets certain
  quality requirements. For example, we check if the CLA is signed, PR has
  sufficient description, if applicable unit tests are added, if it is a
  reasonable contribution (meaning it is not a single liner cosmetic PR).

**2. Valid?**

-   If the PR passes all the quality checks then we go ahead and assign a
    reviewer.
-   If the PR didn't meet the validation criteria, we request for additional
    changes to be made to PR to pass quality checks and send it back or on a
    rare occasion we may reject it.

**3. Review**

-   For a valid PR, reviewer (person familiar with the code/functionality)
    checks if the PR looks good or needs additional changes.
-   If all looks good, the reviewer will approve the PR.
-   If a change is needed, the contributor is requested to make the suggested
    change.
-   You make the change and submit it for the review again.
-   This cycle repeats itself until the PR gets approved.
-   Note: As a friendly reminder, we may reach out to you if the PR is awaiting
    your response for more than 2 weeks.

**4. Approved**

-   Once the PR is approved, it gets `kokoro:force-run` label applied and it
    initiates CI/CD tests.
-   We can't move forward if these tests fail.
-   In such situations, we may request you to make further changes to your PR
    for the tests to pass.
-   Once the tests pass, we now bring all the code into the internal code base,
    using a job called "copybara".

**5. Copy to Google Internal codebase and run internal CI**

-   Once the PR is in the Google codebase, we make sure it integrates well with
    its dependencies and the rest of the system.
-   Rarely, If the tests fail at this stage, we cannot merge the code.
-   If needed, we may come to you to make some changes. At times, it may not be
    you, it may be us who may have hit a snag. Please be patient while we work
    to fix this.
-   Once the internal tests pass, we go ahead and merge the code internally as
    well as externally on GitHub.

In a graphical form, the entire lifetime of a PR looks like

![image](https://github.com/tensorflow/tensorflow/assets/52792999/3eea4ca5-daa0-4570-b0b5-2a2b03a724a3)
