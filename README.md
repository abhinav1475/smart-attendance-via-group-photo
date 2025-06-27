# Smart Attendance System Using Group Photo-Based Face Recognition

An AI-driven smart attendance solution that automates student attendance through a single classroom group photo. This system leverages deep learning–based face detection (MTCNN) and recognition (ArcFace) to mark attendance efficiently, robustly, and with minimal user intervention.

---

## 🔍 Overview

Manual roll-call systems consume 5–10 minutes per class and are prone to proxy attendance. Our system enables faculty to simply take a **group photo**, upload it to the CMS portal with class and time metadata, and **automatically mark attendance** using facial recognition. It operates effectively in varied lighting and angle conditions.

This project achieved **over 92% accuracy** on real-world classroom data and **95% on LFW benchmark** with support for scalability, minimal human input, and dynamic class handling.

---

## 🧠 Core Technologies

- **Face Detection:** MTCNN (Multi-task Cascaded Convolutional Networks)
- **Face Recognition:** ArcFace (Additive Angular Margin Loss)
- **Similarity Metric:** Cosine Similarity
- **Preprocessing & Augmentation:** Histogram Equalization, Rotation, Brightness Variation
- **Implementation:** Python, TensorFlow, Keras, OpenCV
- **Platform:** Google Colab

---

## 📁 Project Structure

This repository includes **4 key Colab notebooks**:

1. ### `01_Face_Dataset_Generation.ipynb`
   - Detects and extracts face crops from student passport-size photographs using MTCNN.
   - Saves cropped images with student labels to create the base dataset.

2. ### `02_Data_Augmentation.ipynb`
   - Applies data augmentation (rotation, flipping, brightness changes, etc.) to simulate real-world variations.
   - Enhances dataset robustness for better generalization.

3. ### `03_ArcFace_Training.ipynb`
   - Trains an ArcFace-based recognition model on the augmented dataset.
   - Generates facial embeddings and saves them along with student labels.

4. ### `04_Recognise_Faces_Group_Image.ipynb`
   - Detects faces in uploaded group photos.
   - Compares them with the pre-trained embeddings using cosine similarity.
   - Outputs attendance results including name tags on recognized faces.

---

## 📊 Performance Highlights

- 📸 Tested on real group photos of **23 students**
- 🧠 Achieved:
  - **Accuracy:** 92%
  - **Precision:** 91%
  - **Recall:** 93%
  - **F1 Score:** 0.92
- 🧪 LFW Dataset Accuracy: **95%**
- 🖼️ Supports group images with varying lighting, angles, and occlusions

---

## 🖥️ System Workflow

1. Teacher uploads a classroom group photo via CMS
2. System detects all visible faces using **MTCNN**
3. Extracts ArcFace embeddings and compares them using **cosine similarity**
4. Attendance is marked and results are displayed with overlays on faces
5. Logs are stored with timestamps for administrative review

---

## 📌 Research Paper

📄 A complete research paper describing the methodology, experiments, and comparisons is included in this repository as `Manuscript_1.pdf`.

**Title:** Automated Attendance Monitoring Using Group Photo-Based Face Recognition  
**Authors:** Abhinav Garlapati, Pavan Kumar, Shiva Shankar Reddy, Mrs. V. Lavanaya

---

## 🚀 Future Work

- Add liveliness detection to prevent spoofing
- Optimize for low-power devices (mobile & edge)
- Expand to handle crowd occlusions and larger datasets
- Encrypt student images and attendance logs for security

---

## 🤝 Contributors

- [Abhinav Garlapati](mailto:abhinavgarlapatik@gmail.com)  
- [Pavan Kumar Challapalli](mailto:228w1a5412@vrsec.ac.in)  
- [Shiva Shankar Reddy Tara](mailto:tarashiva20@gmail.com)  
- [Mrs. V. Lavanaya (Mentor)](mailto:lavanaya@example.com)

---

## 📌 Citation

If you use this work in your academic research, please cite the accompanying paper or contact the authors.

---

## 📷 Sample Output

- ✔️ Detected faces with name overlays  
- 🕒 Timestamped logs  
- ❌ Unrecognized faces flagged for manual review
  

---

## 🔒 License

This project is for academic and research use only. Commercial use is restricted unless permitted by the authors.

---

