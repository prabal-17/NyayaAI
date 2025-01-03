# Legal Case Analysis Tool (BNS 2023)

This project is a **Legal Case Analysis Tool** designed to assist judges, lawyers, and police officers by providing case-specific legal guidance based on the **Bharatiya Nyaya Sanhita (BNS) 2023**. Built using **Gradio** and **Google Vertex AI**, this tool provides precise legal sections and punishments relevant to Indian criminal law.

## **Project Overview**
The tool integrates advanced generative AI models to analyze legal documents and case descriptions. It references the latest Indian criminal code and provides insights into legal sections, applicable punishments, and procedural guidance.

### **Key Features**
- Utilizes **Vertex AI's generative model** for legal content generation.
- Reads and interprets PDF documents containing legal texts.
- Provides legal analysis based on **BNS 2023**.
- Implements **exponential backoff with jitter** for robust API handling.
- Offers an intuitive **Gradio interface** for user input.

---

## **Installation and Setup**
### **1. Clone the Repository**
```bash
git clone https://github.com/yourusername/NyayaAI.git
cd legal-case-analysis-bns
```

### **2. Install Required Packages**
```bash
pip install gradio google-cloud-storage google-cloud-aiplatform
```

### **3. Configure Vertex AI Credentials**
This tool requires **Google Cloud credentials** to access Vertex AI services. Use the Kaggle Secrets API to manage credentials:
```python
from kaggle_secrets import UserSecretsClient
user_secrets = UserSecretsClient()
user_credential = user_secrets.get_gcloud_credential()
user_secrets.set_tensorflow_credential(user_credential)
```

### **4. Launch the Gradio Interface**
```bash
python app.py
```
The Gradio interface will launch locally. Use the provided link to access it in your browser.

---

## **Usage Instructions**
1. Enter a **case description** in the text box.
2. Click **Submit** to get a detailed legal analysis.
3. The tool will return relevant sections from the **Bharatiya Nyaya Sanhita (BNS) 2023** and offer case-specific insights.

---

## **Project Structure**
```
legal-case-analysis-bns/
├── app.py                # Main application file
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
└── /assets               # Images and PDFs
```

---

## **Key Components**
- **Gradio Interface**: Provides a user-friendly interface to interact with the tool.
- **Vertex AI**: Utilized for generating legal analysis content.
- **Safety Settings**: Configured to manage content safety and ensure reliable responses.

### **Exponential Backoff with Jitter**
The tool implements an **exponential backoff with jitter** mechanism to handle API request failures gracefully.

---

## **Example Output**
```text
Legal Analysis:
Section 302: Punishment for murder
Explanation: Any person who commits murder shall be punished with death or imprisonment for life.
```

---

## **Links to Project Resources**
- **Project Repository**: [GitHub Repository Link](https://github.com/yourusername/legal-case-analysis-bns)
- **Gradio Interface**: [Live Demo Link](https://gradio.app/demo)
- **Legal Document (BNS 2023)**: [PDF Document Link](https://yourlink.com/a2023-45.pdf)

---

## **Images and Assets**
- **Interface Screenshot**: [Interface Image Link](nyayaAi.png)

---

## **Future Enhancements**
- Integration with **Supabase** for user authentication.
- Adding more detailed legal texts and case studies.
- Multi-language support for regional languages in India.

---

## **Contributors**
- **Your Name** - [GitHub Profile](https://github.com/yourusername)

## **License**
This project is licensed under the MIT License. See the LICENSE file for details.

