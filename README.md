# Project_1
For Datawarehouse And Big Data Analytics 
## Group_6
### สมาชิก
1. 673020252-4 นางสาวณิรดา อนุนิวัฒน์

2. 673020258-2 นางสาวปวริศา โง่นสูงเนิน

3. 673020265-5 นางสาวสุพิชชา คำสิงห์

4. 673020262-1 นายวรวัฒน์ พรหมคุณ

5. 673020247-7 นายชวนากร เพชรเจริญรัตน์
   
## Part 2: Voice of Customer จากรีวิว Amazon
### dataset
https://drive.google.com/drive/folders/1hBu5Mwy-m_gt-76fdwrLA0322evUUj_0?usp=drive_link
## อธิบายโปรเจค
## 1. Project Overview

โปรเจคนี้มีวัตถุประสงค์เพื่อประยุกต์ใช้เทคนิค Text Analytics
ในการวิเคราะห์ข้อมูลรีวิวของลูกค้า เพื่อค้นหา Pattern
และ Business Insight ที่สามารถนำไปใช้สนับสนุนการตัดสินใจทางธุรกิจได้

สำหรับ Part 2: Voice of Customer (VoC)
ทีมเลือกใช้ข้อมูลรีวิวจาก Amazon Reviews 2023
ในหมวด **Musical Instruments** เพื่อวิเคราะห์ความคิดเห็น
และประสบการณ์ของลูกค้าที่มีต่อสินค้า

---

## 2. Objectives

วัตถุประสงค์ของ Part 2 มีดังนี้

1. ตรวจสอบและเตรียมข้อมูล Amazon Reviews
   และ Product Metadata ให้พร้อมสำหรับการวิเคราะห์
2. วิเคราะห์ความคิดเห็นของลูกค้าจากรีวิวสินค้าในหมวด Musical Instruments
3. ประยุกต์ใช้ Text Analytics เพื่อสกัดข้อมูลและ Pattern
   จากข้อความรีวิว
4. นำผลการวิเคราะห์มาสร้าง Business Insights
   ที่สามารถนำไปใช้ประโยชน์ทางธุรกิจได้
## 3. Dataset

### Dataset: Musical_Instruments

โปรเจคนี้ใช้ข้อมูล **Amazon Reviews 2023** ในหมวด
**Musical_Instruments** โดยใช้ข้อมูล 2 ส่วน ได้แก่ Review Data
และ Product Metadata ซึ่งนำมาเชื่อมกันด้วย `parent_asin`

### 3.1 Review Data

Review Data ประกอบด้วย 4 columns ได้แก่

| Column | Data Type | Description |
|---|---|---|
| `user_id` | object | รหัสผู้ใช้งาน |
| `parent_asin` | object | รหัสสินค้า |
| `rating` | float64 | คะแนนรีวิว |
| `timestamp` | int64 | เวลาที่ทำการรีวิว |

**จำนวนข้อมูล:** 2,975,551 reviews

### 3.2 Product Metadata

Product Metadata ประกอบด้วย 14 columns ได้แก่

| Column | Data Type |
|---|---|
| `main_category` | object |
| `title` | object |
| `average_rating` | float64 |
| `rating_number` | int64 |
| `features` | object |
| `description` | object |
| `price` | float64 |
| `images` | object |
| `videos` | object |
| `store` | object |
| `categories` | object |
| `details` | object |
| `parent_asin` | object |
| `bought_together` | float64 |

**จำนวนข้อมูล:** 213,593 product metadata records

### 3.3 Data Integration

Review Data และ Product Metadata ถูกเชื่อมเข้าด้วยกัน
โดยใช้ `parent_asin` เป็น key เพื่อให้สามารถนำข้อมูลรีวิว
มาเชื่อมกับข้อมูลรายละเอียดของสินค้าได้

---

