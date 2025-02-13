# **YouTube Data Analysis and Sentiment Insights 📊📈**

## **Overview**
This repository contains a set of Jupyter notebooks and scripts for **extracting YouTube comments, analyzing sentiment, and tracking video engagement metrics** over time. By automating data collection and sentiment analysis, this project helps in understanding audience engagement and reactions to videos.

---

## **Project Structure 📁**
The repository consists of the following main scripts:

### **1️⃣ Extracting Video IDs & Comments (`Extracting VideoIDs+Comments.ipynb`)**
- This script allows users to **enter YouTube video URLs** and automatically **extract video IDs**.
- It securely retrieves comments using the **YouTube Data API**.
- The API key is entered separately to ensure secure usage.

### **2️⃣ Secure API Key Handling (`get pass.ipynb`)**
- This script prompts users to **enter their YouTube API key securely**.
- The API key is then used in subsequent scripts to fetch YouTube comments and metadata.

### **3️⃣ Engagement Metrics Tracking (`TaskScheduler.ipynb`)**
- This script **tracks video engagement statistics** at a given time.
- It pulls:
  - 📌 **Views**
  - 📌 **Likes**
  - 📌 **Comments Count**
- The script is **designed to be run automatically** using Windows **Task Scheduler**.
- The output is **stored as a CSV file** at the specified file location.
- Since all data files share the **same columns**, they can be concatenated later to observe trends over time.

### **4️⃣ Sentiment Analysis (`Sentiment Analysis.ipynb`)**
- This script **performs sentiment analysis** on YouTube comments using a **pre-trained model from Hugging Face**.
- It assigns **sentiment scores and sentiment tags** to each comment.
- The script then **analyzes sentiment trends** and generates:
  - 📊 **Hourly sentiment trends**
  ![image](https://github.com/user-attachments/assets/b925586c-d942-47ab-bcad-999c8a3f3c1a)

  - 📈 **Comment engagement trends**
  - ☁️ **Word clouds for key discussion topics**
  ![image](https://github.com/user-attachments/assets/a3886234-4cd7-4175-a4f9-1f8a3d24b599)

  - ⭐ **Star rating distributions based on sentiment**
![image](https://github.com/user-attachments/assets/a69f4492-4da5-41e9-83f8-b773fcaabda6)

---

## **Setup & Usage 🚀**
### **📌 Prerequisites**
Ensure you have the following installed:
- **Python 3.x**
- **Jupyter Notebook**
- **Required Python Libraries**:
  ```bash
  pip install pandas numpy requests google-auth google-auth-oauthlib google-auth-httplib2 googleapiclient transformers wordcloud matplotlib seaborn
