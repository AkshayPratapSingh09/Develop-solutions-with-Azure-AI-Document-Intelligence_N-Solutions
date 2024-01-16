# Develop-solutions-with-Azure-AI-Document-Intelligence_N-Solutions
<a href="https://learn.microsoft.com/en-us/training/challenges?id=56b0afce-3a58-4fb5-a3d0-79da518fd84c&WT.mc_id=cloudskillschallenge_56b0afce-3a58-4fb5-a3d0-79da518fd84c">Develop solutions with Azure AI Document Intelligence_N</a>

## Azure AI Document Intelligence Q&A

### 1. You want to create an Azure AI Document Intelligence model where the documents are in one of three formats: wills, probate declarations, and affidavits. Each has their own specific layout. What type of model should you use that will understand the format of the three document categories?

- A Read model.
- A Layout model.
- A Composed model.

**Correct.** A Composed model consists of multiple custom models. Each submitted form is categorized as one of the custom form types and analyzed using the corresponding custom model.

### 2. You have developed a custom model that analyzes health assessment forms returned by patients to a medical practice. You've observed too much inaccuracy in the values that the model extracts for each field. What should you do to address this problem?

- Retrain the model with a larger number of example forms.
- Change from a custom model to the general document model.
- Change from the free tier to the standard tier.

**Correct.** The larger the number of example forms you use to train a model, the more accurate it will be and the higher the confidence levels will be.

### 3. You want to call your Azure AI Document Intelligence solution from a mobile app by using an API. Which of the following programming languages is natively supported as an Azure AI Document Intelligence SDK?

- Python
- Go
- R

**Correct.** Microsoft publishes a Python API you can use to call Azure AI Document Intelligence services.

### 4. You're building a solution that analyzes sales invoices. You expect to receive up to 10 concurrent requests at busy times and you want your solution to be as simple as possible. What kind of resource should you create?

- A Free tier Azure AI Document Intelligence resource.
- A Standard tier Azure AI Document Intelligence resource.
- An Azure AI Services multi-service resource.

**Correct.** The Standard tier supports up to 15 concurrent requests, and you don't need other Azure AI Services.

### 5. Which of the following is an Azure AI Document Intelligence prebuilt model?

- Employment record
- Resume
- Receipt

**Correct.** The receipt model can identify commonly used fields and their values in scanned or photographed receipt documents.


1. You have a large set of documents with varying structures that contain customer name and address information. You want to extract entities for each customer. Which prebuilt model should you use? 

- Read model.
  **Incorrect.** The read model can extract text and identify languages but doesn't support entity extraction.

- General document model.
  **Correct.** The general document model is the only one that supports entity extraction.

- ID document model.

2. You are using the prebuilt layout model to analyze a document with many checkboxes. You want to find out whether each box is checked or empty. What object should you use in the returned JSON code? 

- Selection marks.
  **Correct.** Selection marks record checkboxes and radio buttons and include whether they're selected or not.

- Bounding boxes.

- Confidence indicators.

3. You submit a Word document to the Azure AI Document Intelligence general document model for analysis but you receive an error. The file is A4 size, contains 1 MB of data, and is not password-protected. How should you resolve the error? 

- Change from the free tier to the standard tier.

- Submit the document one page at a time.

- Convert the document to PDF format.
  **Correct.** Word documents are not supported by Azure AI Document Intelligence but PDF documents are supported. Azure AI Document Intelligence is designed to analyze scanned and photographed paper documents, not documents that are already in a digital format, so you should consider using another technology to extract the data in Word documents.


