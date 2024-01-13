# Chat-with-Database-using-LangChain
### <b> Chat with your Database using LangChain Framework </b>

## System Setup:
Step 1. Create a virtual environment
  > conda create -p myenv python=3.9 -y

step 2. Activate the environment:
  > conda activate myenv/

step 3. Install all the requirements:
  > pip install -r requirements.txt
 
step 4. start writing the code, with standard file name as main.py

## <b> Flow </b>
![image](https://github.com/Chandrakant817/Chat-with-Database-using-LangChain/assets/69152112/7e86e78e-c6cb-4f9d-b60f-a8a8d12f98ce)

### </b> ‘Talk’ to Your Database[MySQL, SQL, or Azure Sql] Using LangChain and GenerativeAI Models </b>

LangChain is an open-source library that offers developers a comprehensive set of resources to develop applications that run on Large Language Models (LLMs) by establishing a mechanism for linking LLMs to external data sources, such as SQL Databases, personal documents or the internet. Developers can utilize LangChain to string together a sequence of commands to create sophisticated applications.
LangChain are compatible Delta Taables, MySQL, PostgreSQL, Oracle SQL and SQLite.
LangChain Structure:
The framework is organized into seven modules. Each module allows you to manage a different aspect of the interaction with the LLM.
§ LLM, Chains, prompts, Document Loaders and Utils, agents or sql chains, Indexes and Memory to build and run SQL queries.
LangChain SQL Chains:
It represents a SQL database chain and implements the functionality to generates SQL queries like Table Info and column information as well as sample data from the table. To mitigate risk of leaking sensitive data, limit permissions to read and scope to the tables are needed.

#### LangChain Agent:
An Agent Executor is a runnable interface of the Agent and its set of Tools. The agent executor is responsible for calling the agent, getting the action and action input, calling the tool that the action references with the corresponding input, getting the output of the tool, and then passing all that information back into the Agent to get the next action it should take. Usually it is an iterative process until the Agent reaches the Final Answer or output.
SQL Agent could perform DML operations(insert, update or delete operations) on your database based on specific questions.
One way to ensure that any accidental DML operation does not happen is to create a database user with only read access.

#### LangChain SQL Use Cases:
§ Build SQL queries based on natural language user questions
§ Query a SQL database using chains for query creation and execution
§ Interact with a SQL database using agents for robust and flexible querying

#### Improvements:
§ Customizing database description
§ Hardcoding a few examples of questions and their corresponding SQL query in the prompt
§ Using a vector database to include dynamic relevant examples
§ Adding sample rows
§ Specifying custom table information
This Sequential Chain handles the process of:
§ Determining which tables to use based on the user question
§ Calling the normal SQL database chain using only relevant tables
§ Customizing the LLM Prompt include specific instructions or relevant information
§ Get intermediate steps access the SQL statement as well as the final result
§ Limit the number of rows a query will return

#### SQL agents
- Enhanced Flexibility for interacting with SQL.
- Schema and Content Interaction
- Descriptive Capabilities: Describe specific tables, providing detailed insights.
- Error Recovery
