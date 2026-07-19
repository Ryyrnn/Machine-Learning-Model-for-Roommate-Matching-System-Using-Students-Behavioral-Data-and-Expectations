# Machine-Learning-Model-for-Roommate-Matching-System-Using-Students-Behavioral-Data-and-Expectations
การพัฒนาโมเดล Machine Learning สำหรับระบบจับคู่รูมเมท โดยใช้ข้อมูลพฤติกรรมและความคาดหวังของนักศึกษา : กรณีศึกษานักศึกษามหาวิทยาลัยธรรมศาสตร์ ศูนย์รังสิต

โครงงานวิจัยนี้มีวัตถุประสงค์เพื่อพัฒนาโมเดล Machine Learning สำหรับระบบจับคู่เพื่อนร่วมห้อง โดยใช้ข้อมูลพฤติกรรมและความคาดหวังของนักศึกษามหาวิทยาลัยธรรมศาสตร์ ศูนย์รังสิต เพื่อช่วยลดปัญหาความขัดแย้งที่อาจเกิดขึ้นจากการใช้ชีวิตร่วมกันในหอพัก เช่น ความแตกต่างด้านเวลานอน ความสะอาด การสูบบุหรี่ การใช้พื้นที่ส่วนตัว และรูปแบบการสื่อสาร ซึ่งล้วนส่งผลต่อคุณภาพชีวิตและความสัมพันธ์ระหว่างเพื่อนร่วมห้อง
การเก็บรวบรวมข้อมูลจากนักศึกษาที่พักอาศัยที่หอในมหาวิทยาลัยธรรมศาสตร์ ศูนย์รังสิต ดำเนินการผ่านแบบสอบถามออนไลน์ โดยแบ่งข้อมูลออกเป็น 2 ส่วน ได้แก่ ข้อมูลด้านพฤติกรรมและไลฟ์สไตล์ของผู้ตอบแบบสอบถาม (Profile) และข้อมูลด้านความคาดหวังต่อเพื่อนร่วมห้อง (Expectation) จากนั้นนำข้อมูลมาผ่านกระบวนการเตรียมข้อมูล ประกอบด้วย Feature Selection, Encoding และ Feature Scaling เพื่อให้เหมาะสมต่อการวิเคราะห์ด้วย Machine Learning
ในการวิเคราะห์ข้อมูล ผู้วิจัยได้ใช้เทคนิค K-Means Clustering เพื่อจัดกลุ่มนักศึกษาที่มีลักษณะพฤติกรรมและความคาดหวังใกล้เคียงกัน โดยกำหนดจำนวนกลุ่มที่เหมาะสมจากการพิจารณาร่วมกันระหว่าง Elbow Method และ Silhouette Score ซึ่งพบว่าค่า k = 6 มีความเหมาะสมที่สุด ผลลัพธ์สามารถจำแนกกลุ่มนักศึกษาออกเป็น 6 กลุ่มหลักที่มีลักษณะด้านบุคลิกภาพ พฤติกรรมการนอน และรูปแบบการใช้ชีวิตแตกต่างกันอย่างชัดเจน
หลังจากการจัดกลุ่ม ผู้วิจัยได้นำเทคนิค Cosine Similarity มาใช้วัดระดับความคล้ายคลึงระหว่างผู้ใช้งานภายใน Cluster เดียวกัน เพื่อค้นหาคู่เพื่อนร่วมห้องที่มีแนวโน้มเข้ากันได้สูง โดยพิจารณาจากทั้งข้อมูลพฤติกรรมและความคาดหวังร่วมกัน
ผลการศึกษาพบว่า ปัจจัยที่มีอิทธิพลต่อการเลือกเพื่อนร่วมห้องมากที่สุด ได้แก่ พฤติกรรมการสูบบุหรี่ ความสะอาด ช่วงเวลานอน และรูปแบบการสื่อสาร อีกทั้งผู้ตอบแบบสอบถามส่วนใหญ่มีแนวโน้มต้องการเพื่อนร่วมห้องที่มีลักษณะใกล้เคียงกับตนเอง งานวิจัยนี้แสดงให้เห็นว่า การประยุกต์ใช้เทคนิค Machine Learning สามารถช่วยสนับสนุนการพัฒนาระบบจับคู่เพื่อนร่วมห้องได้อย่างมีประสิทธิภาพ และสามารถนำไปต่อยอดใช้งานจริงเพื่อช่วยลดความขัดแย้งและส่งเสริมคุณภาพชีวิตในการอยู่อาศัยร่วมกันในหอพักนักศึกษาได้ในอนาคต

คำสำคัญ: K-means, Cosine Similarity, Profile, Expectation, เพื่อนร่วมห้อง


## Files

- **Python_Project.ipynb** : Source code of the project
- **Dataset Roommate.xlsx** : Dataset used in the project

---

## Google Colab

https://colab.research.google.com/drive/1CkQjIQle7CqrSY96jR0dRbUlg6bsKH_a#scrollTo=q57jAzmHGIg5

---

## How to Run

1. Download **Python_Project.ipynb** from this repository.

2. Download **Dataset Roommate.xlsx** from this repository.

3. Open **Python_Project.ipynb** using **Google Colab**.

4. Upload **Dataset Roommate.xlsx** to the Colab working directory (Files panel on the left).

5. Verify that the dataset filename matches the filename referenced in the notebook.

6. Run all notebook cells sequentially from top to bottom.

7. Wait for the preprocessing, clustering, and similarity calculations to complete.

8. View the clustering and roommate matching results.
