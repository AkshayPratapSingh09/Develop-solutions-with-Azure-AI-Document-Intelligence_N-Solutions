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


### 1. You have a large set of documents with varying structures that contain customer name and address information. You want to extract entities for each customer. Which prebuilt model should you use? 

- Read model.
  **Incorrect.** The read model can extract text and identify languages but doesn't support entity extraction.

- General document model.
  **Correct.** The general document model is the only one that supports entity extraction.

- ID document model.

### 2. You are using the prebuilt layout model to analyze a document with many checkboxes. You want to find out whether each box is checked or empty. What object should you use in the returned JSON code? 

- Selection marks.
  **Correct.** Selection marks record checkboxes and radio buttons and include whether they're selected or not.

- Bounding boxes.

- Confidence indicators.

### 3. You submit a Word document to the Azure AI Document Intelligence general document model for analysis but you receive an error. The file is A4 size, contains 1 MB of data, and is not password-protected. How should you resolve the error? 

- Change from the free tier to the standard tier.

- Submit the document one page at a time.

- Convert the document to PDF format.
  **Correct.** Word documents are not supported by Azure AI Document Intelligence but PDF documents are supported. Azure AI Document Intelligence is designed to analyze scanned and photographed paper documents, not documents that are already in a digital format, so you should consider using another technology to extract the data in Word documents.


### 1. A person plans to use an Azure Document Intelligence prebuilt invoice model. To extract document data using the model, what are two calls they need to make to the API?

- Train Model and Get Model Labels

- Analyze Invoice and Get Analyze Invoice Result

**Correct:** The Analyze Invoice function starts the form analysis and returns a result ID, which they can pass in a subsequent call to the Get Analyze Invoice Result function to retrieve the results.

- Create Azure Document Intelligence and Get Analyze Invoice Result

### 2. A person needs to build an application that submits expense claims and extracts the merchant, date, and total from scanned receipts. What's the best way to do this?

- Use the Read API of the Computer Vision service.

- Use Azure Document Intelligence's prebuilt receipts model

**Correct:** Use the Azure Document Intelligence's prebuilt receipts model. It can intelligently extract the required fields even if the scanned receipts have different names in them.

- Use Azure Document Intelligence's Layout service

### 3. A person is building a custom model with Azure Document Intelligence services. What is required to train a model?

- Along with the form to analyze, JSON files need to be provided.

**Correct:** The labels needed in training are referenced in the ocr.json files, labels.json files, and single fields.json file.

- Training must be done through language specific SDKs.

- Nothing else is required.


## 1. You have a composed model that consists of three custom models. You're writing code that sends forms to the composed model, and you need to check which of the custom models was used to analyze each form. Which property should you use from the returned JSON?

- modelId.

- status.

- docType.

**Correct.** The docType property includes the model ID of the custom model that was used to analyze the document.

## 2. You're trying to create a composed model, but you're receiving an error. Which of the following should you check?

- That the custom models were trained with labels.

**Correct.** Only custom models that have been trained with labeled example forms can be added to a composed model.

- That the custom models all have the same model ID.

- That the custom models all have the same list of fields.

## 1. Which of the following values does Cognitive Search use to match a form submitted to a custom skill with the right response from that skill?

- formUrl.

- recordId.

**Correct.** The recordId value in the output is matched to the recordId of a form in the input.

- formSasToken.

## 2. You're troubleshooting your Cognitive Search indexing process. You have a single custom skill that calls Azure AI Document Intelligence, but requests are never received by your skill. Which of the following stages of the indexing process might be causing the problem?

- Push to index.

- Output field mapping.

- Document cracking.

**Correct.** Since the document cracking stage happens before the skillset execution, it might prevent requests from reaching your custom skill.



## 1. You want to create a knowledge base from an existing FAQ document. What should you do?

- Create an empty knowledge base and manually enter the FAQ questions and answers.

- Create a new knowledge base, importing the existing FAQ document.
  **Correct.** You can create a knowledge base from an existing document or web page.

- Create a new knowledge base, selecting only the Professional chit-chat source.

## 2. How can you add a multi-turn context for a question in an existing knowledge base?

- Add synonyms to the knowledge base.

- Add alternative phrasing to the question.

- Add a follow-up prompt to the question.
  **Correct.** To add a multi-turn context to a question, define a follow-up prompt.

## 3. How can you enable users to use your knowledge base through email?

- Add Friendly Chit-chat to the knowledge base.

- Enable Active Learning for the knowledge base and include the user's email address as the userId parameter in responses.

- Create a bot based on your knowledge base and configure an email channel.
  **Correct.** You can create a bot for your published knowledge base and configure a channel for email communication.


  ## 1. How should you create an application that monitors the comments on your company's website and flags any negative posts?

- Use the Azure AI Language service to extract key phrases.

- Use the Azure AI Language service to perform sentiment analysis of the comments.
  **Correct.** Sentiment analysis helps you determine if text is negative or positive.

- Use the Azure AI Language service to extract named entities from the comments.

## 2. You have analyzed text that contains the word "Paris". How might you determine if this word refers to the French city or the character in Homer's "The Iliad"?

- Use the Azure AI Language service to extract key phrases.

- Use the Azure AI Language service to detect the language of the text.

- Use the Azure AI Language service to extract linked entities.
  **Correct.** Linked entities enable you to disambiguate common entities of the same name.


## 1. You want to train a model to classify book summaries by their genre, and some of your favorite books are both mystery and thriller. Which type of project should you build?

- A single label classification project

- A multiple label classification project
  **That answer's correct.** Use a multiple label classification project to label books as multiple genres.

- A varied label classification project

## 2. You just got notification your training job is complete. What is your next step?

- Label more data

- Deploy your model

- View your model details
  **That answer's correct.** First view your model details to see how it scored, the classification distribution, and where it needs improvement.

## 3. You want to submit a classification task via the API. How do you get the results of the classification?

- The result is in the response of the classification request.

- Call an endpoint with your deployment name to get the most recent classification.

- Call the URL provided in the header of the request response.
  **That answer's correct.** Get the value from the operation-location header in the request response, and use that to retrieve the results of the classification request.


## 1. You've trained your model and you're seeing that it doesn't recognize your entities. What metric score is likely low to indicate that issue?

- Recall
  **That answer's correct.** Recall indicates how well the model extracts entities, regardless of which entity that is.

- Precision

- F1 score

## 2. You just finished labeling your data. How and where is that file stored to train your model?

- JSON file, in my storage account container for the project
  **That answer's correct.** The JSON file lives next to the dataset in your container for the model to use during training.

- XML file, in my local project folder

- YAML file, anywhere in my Azure account

## 3. You train your model with only one source of documents, even though real extraction tasks will come from several sources. What data quality metric do you need to increase?

- Distribution

- Accuracy

- Diversity
  **That answer's correct.** Having the right data diversity will lead to better extraction performance.


## 1. Your app must interpret a command such as "turn on the light" or "switch the light on". What do these phrases represent in a language model?

- Intents.

- Utterances.
  **That's correct.** Utterances are example phrases that indicate a specific intent.

- Entities.

## 2. Your app must interpret a command to book a flight to a specified city, such as "Book a flight to Paris." How should you model the city element of the command?

- As an intent.

- As an utterance.

- As an entity.
  **That's correct.** The city is an entity to which the intent (booking a flight) should be applied.

## 3. Your language model needs to detect an email when present in an utterance. What is the simplest way to extract that email?

- Use Regular Expression entities.

- Use prebuilt entity components.
  **That's correct.** When a language model needs to detect a common entity, use prebuilt components to have the Azure AI Language service automatically detect the entity.

- Use Learned entity components.


## 1. What function of Azure AI Translator should you use to convert the Chinese word "你好" to the English word "Hello"?

- Detect

- Translate
  **Correct.** Translation converts text from one language to another.

- Transliterate

## 2. What function of Azure AI Translator should you use to convert the Russian word "спасибо" in Cyrillic characters to "spasibo" in Latin characters?

- Detect

- Translate

- Transliterate
  **Correct.** Transliteration converts text from one script to another.

## 3. What function of the Azure AI Translator service should you use to convert the Chinese word "你好" to the English word "Hello"?

- detect

- translate
  **Correct.** Translation converts text from one language to another.

- transliterate

## 4. What function of the Azure AI Translator service should you use to convert the Russian word "спасибо" in Cyrillic characters to "spasibo" in Latin characters?

- detect

- translate

- transliterate
  **Correct.** Transliteration converts text from one script to another.


## 1. What information do you need from your Azure AI Speech service resource to consume it using the Azure AI Speech SDK?

- The location and one of the keys
  **Correct.** The Azure AI Speech SDK requires the location and a key to connect to the Azure AI Speech service.

- The primary and secondary keys

- The endpoint and one of the keys
  **Incorrect.** The Azure AI Speech SDK requires the location and a key to connect to the Azure AI Speech service.

## 2. Which object should you use to specify that the speech input to be transcribed to text is in an audio file?

- SpeechConfig

- AudioConfig
  **Correct.** Use an AudioConfig to specify the input source for speech.

- SpeechRecognizer

## 3. How can you change the voice used in speech synthesis?

- Specify a SpeechSynthesisOutputFormat enumeration in the SpeechConfig object.

- Set the SpeechSynthesisVoiceName property of the SpeechConfig object to the desired voice name.
  **Correct.** To set a voice, set the SpeechSynthesisVoiceName property of the SpeechConfig to a voice name, such as "en-GB-George".

- Specify a filename in the AudioConfig object.

