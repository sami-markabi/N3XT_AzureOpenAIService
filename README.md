<img src="https://www.n3xtsports.com/wp-content/uploads/2021/01/N3XT-Sports-Logo-Colored-Stickyx2.png" alt="N3XTSPORTS" width="120" height="50"/>
# Azure OpenAI Service - N3XTSPORTS



###
## What is Azure OpenAI Service?
Azure OpenAI Service provides REST API access to OpenAI's powerful language models including the GPT-4 (new) and GPT-3 model series. 
###
#### Benefits
* Add our own data source, and be able to chat with it using OpenAI ChatGPT. 
* Easily integrate it with our PowerApps or any WebApps using the deployment feature on Azure.
* Azure OpenAI on your data enables you to run supported chat models such as ChatGPT and GPT-4 on your data without needing to train or fine-tune models. 
###
#### How it works 
* Azure connects to OpenAI API and provides access to the model's text-in, text-out interface.
* Azure OpenAI processes text by breaking it down into tokens. The total number of tokens processed in a given request depends on the length of your input, output and request parameters.
* One of the key features of Azure OpenAI on your data is its ability to retrieve and utilize data in a way that enhances the model's output. Azure OpenAI on your data, together with Azure Cognitive Search, determines what data to retrieve from the designated data source based on the user input and provided conversation history. This data is then augmented and resubmitted as a prompt to the OpenAI model, with retrieved information being appended to the original prompt. Although retrieved data is being appended to the prompt, the resulting input is still processed by the model like any other prompt. Once the data has been retrieved and the prompt has been submitted to the model, the model uses this information to provide a completion.
##

  <img src="https://media.licdn.com/dms/image/D4E12AQGaCCKG5_NmdQ/article-cover_image-shrink_600_2000/0/1684402359330?e=2147483647&v=beta&t=Ny5SqpqLOP_YsOdAraT7ZRj2Dt_bF2wmuKkPW17sD_g" alt="Azure OpenAI" width="2000" height="500"/>


  
##

* Azure OpenAI on your data uses an Azure Cognitive Services index to determine what data to retrieve based on user inputs and provided conversation history. 
##
#### Limitations
##
##### *Data formats*
Azure OpenAI on your data supports the following filetypes:
* .txt
* .md
* .html
* Microsoft Word files
* Microsoft PowerPoint files
* PDF
  
##
##### *System Message*
###
Give the model instructions about how it should behave and any context it should reference when generating a response. You can describe the assistant’s personality, what it should and shouldn’t answer, and how to format responses. The system message will be truncated if it's greater than 200 tokens.


For example, if you're creating a chatbot where the data consists of transcriptions of quarterly financial earnings calls, you might use the following system message:

*"You are a financial chatbot useful for answering questions from financial reports. You are given excerpts from the earnings call. Please answer the questions by parsing through all dialogue."*


##
##### *Maximum Response*

The upper limit for Azure OpenAI on Your Data is 1500 tokens. This is equivalent to setting the max_tokens parameter in the API.

##
##### *Pricing*

- Azure OpenAI Service per 1000 tokens.
- Cognitive Search to access your own data.

##
###### Azure OpenAI Service
## 

|         Models          | Per 1,000 tokens |
|-------------------------|------------------|
|         Text-Ada         |   €0.000374 
|      Text-Babbage       |    €0.000468     |
|       Text-Curie        |    €0.001869     |
|      Text-Davinci       |    €0.018682     |
|      Code-Cushman       |    €0.022419     |
|      Code-Davinci       |    €0.093410     |
| ChatGPT (gpt-3.5-turbo) |    €0.001869     |
##
* All Models are similar in terms of capability, with Text-Davinci being the most capable.
* The Uses of the Following Models:
  * Davinci: Complex intent, cause and effect, summarization for audience.
  * Curie: Language translation, complex classification, text sentiment, summarization.
  * Babbage: Moderate classification, semantic search classification
  * Ada: Parsing text, simple classification, address correction, keywords
  * GPT-35-turbo: Similar to Davinci, but less capable.
* Text-Davinci would be the best model for our requirements.
  
#
|          Model ID          |                        Base model Regions                        | Fine-Tuning Regions | Max Request (tokens) | Training Data (up to) |
|----------------------------|------------------------------------------------------------------|---------------------|----------------------|-----------------------|
|       text-curie-001       |              East US, South Central US, West Europe              |         N/A         |        2,049         |       Oct 2019        |
|      text-davinci-002      |              East US, South Central US, West Europe              |         N/A         |        4,097         |       Jun 2021        |
|      text-davinci-003      |                       East US, West Europe                       |         N/A         |        4,097         |       Jun 2021        |
|  gpt-35-turbo1 (ChatGPT)   | East US, France Central, South Central US, UK South, West Europe |         N/A         |        4,096         |       Sep 2021        |

#
* Assuming a Max Request of 4,097 tokens. 
  **Cost per Request = €0.076540154**
#
###### Cognitive Search pricing

|                           |  Free   |                            Basic                            |                          Standard S1                           |                          Standard S2                           |                                              Standard S3                                               |                      Storage Optimized L1                      |                                          Storage Optimized L2                                          |
|---------------------------|---------|-------------------------------------------------------------|----------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
|          Storage          |  50 MB  |                            2 GB                             |                 25 GB (max 300 GB per service)                 |                 100 GB (max 1 TB per service)                  |                                     200 GB (max 2 TB per service)                                      |                  1 TB (max 12 TB per service)                  |                                      2 TB (max 24 TB per service)                                      |
|  Max indexes per service  |    3    |                             15                              |                               50                               |                              200                               |                              200 or 1000/partition in high density1 mode                               |                               10                               |                                                   10                                                   |
|     Scale out limits      |   N/A   | Up to 3 units per service (max 1 partition; max 3 replicas) | Up to 36 units per service (max 12 partition; max 12 replicas) | Up to 36 units per service (max 12 partition; max 12 replicas) | Up to 36 units per service (max 12 partition; max 12 replicas) up to 12 replicas in high density1 mode | Up to 36 units per service (max 12 partition; max 12 replicas) | Up to 36 units per service (max 12 partition; max 12 replicas) up to 12 replicas in high density1 mode |
| Price per SU (Scale Unit) | €0/hour |                         €0.10/hour = 	€68.88/month                          |                           €0.32/hour  = €229.12/month                         |                           €1.26/hour                           |                                               €2.52/hour                                               |                           €3.59/hour                           |                                               €7.18/hour                                               |
##
* Assuming a Basic Cognitive Seach Plan.
  **Cost per Plan = €68.88/month**


#### *Total Cost: €7.6540154/100 Requests & €68.88/month.*
#
#
##### *Other Hard Limitations*


* Default quota per model and region Text-Davinci-003 = 120K tokens per minute ≈ 30 requests/min.
* Total size of all files per resource =	1 GB.

#
#

### How to Implement

#### Prerequisites
* An Azure Subscription.
* Access granted to Azure OpenAI using https://aka.ms/oai/access.
* A database resource with a ***supported format*** either on Azure Blobs, Cognitive Search, or be able to upload it directly.

##

#### Steps to add your data using Azure OpenAI Studio

Navigate to Azure OpenAI Studio and sign-in with credentials that have access to your Azure OpenAI resource. During or after the sign-in workflow, select the appropriate directory, Azure subscription, and Azure OpenAI resource.


1. Create an Azure AI Studio using oai.azure.com.
2. Choose the **N3XT Global Subscription** for the Subscription menu & either choose a resource group or create a new one.
3. Choose **West Europe** for the region and name the resource accordingly. 
4. Choose A **Pricing Tier**: Standard S0

5. Select the **Chat playground tile**.
##
   <img src="https://learn.microsoft.com/en-us/azure/cognitive-services/openai/media/quickstarts/chat-playground-card.png" alt="step1" width="1000" height="300"/>
##

6. Create a **new deployment**. Select a model to use (Text-Davinci).
7. On the **Assistant setup tile**, select **Add your data (preview)** > + Add a data source.


##
   <img src="https://learn.microsoft.com/en-us/azure/cognitive-services/openai/media/quickstarts/chatgpt-playground-add-your-data.png" alt="step1" width="1000" height="300"/>
##


8. In the pane that appears, select **Upload files** or choose an **Azure Blob** under Select data source. Azure OpenAI needs both a storage resource and a search resource to access and index your data. **Make sure to Turn on CORS**.
9. Select your **Azure Cognitive Search** resource or create a new one.
10. Start exploring with the **Chat playground**.



##
   <img src="https://learn.microsoft.com/en-us/azure/cognitive-services/openai/media/quickstarts/chat-playground.png" alt="step1" width="1000" height="400"/>
##

11. Once you're satisfied with the experience in Azure OpenAI studio, you can deploy a web app directly from the Studio by selecting the **Deploy to button**.
