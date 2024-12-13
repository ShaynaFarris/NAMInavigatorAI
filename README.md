# NAMInavigatorAI

## Prerequisites

### Accounts / Accesses required

Follow [these steps](https://platform.openai.com/docs/quickstart#create-and-export-an-api-key) to create an OpenAI API key
  - Save this key somewhere safe. Once it goes away you will not be able to access it again.

Follow [these steps](https://docs.pinecone.io/guides/get-started/quickstart#2-get-an-api-key) to create a Pinecone API key
  - Save this key somewhere safe. Once it goes away you will not be able to access it again.

### Setting up Google CoLab

The easiest way to run the Python Notebook is to upload it into Google CoLab.

Go to [Google CoLab](https://colab.research.google.com/), select **Upload** and **Browse**, then find the [NAMInavigatorAI.ipynb](./NAMInavigatorAI.ipynb) file on your machine.

Click the key icon on the lefthand side of the page. Create new secrets for your two API keys with the following names
  - OPENAI_API_KEY
  - PINECONE_API_KEY
  > Ensure you allow Notebook acccess for them both


### Creating a Pinecone Index

Create a Pinecone Index by following [this link](https://app.pinecone.io/organizations/-OCKCUliNUkdojiW8Lzy/projects/103dfd91-2332-43b0-9c58-881c6ec2624c/indexes) and selecting `Create Index` and using the following parameters:
- Configuration -> text-embedding-3-small
- Capacity mode -> Serverless
- Cloud provider -> aws
- Region -> Virginia

## Running the notebook

1. Update the `index-name` variable values within the last two cells to match the index you created in the previous section.
2. Move or upload any **.txt** documents you want to makeup your knowledge base into a folder in your google drive at the following location: `content/gdrive/MyDrive/NAMInavigaotrAI/use`.
3. Now you should be able to run all the cells in order to:
   1. download dependencies
   2. create your indexes to makeup your knowledge base
   3. start a chat interface to ask questions
  > NOTE: if/when your instance force reloads, just continue running with the next cell.
