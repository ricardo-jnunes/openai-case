# openai-study


### Large language models 
Large language models (LLMs) are deep learning algorithms that can recognize, summarize, translate, predict, and generate content using very large datasets. LLMs largely represent a class of deep learning architectures called transformer networks. A transformer model is a neural network that learns context and meaning by tracking relationships in sequential data, like the words in this sentence.

LLM are stateless, so far a conversation, the chat is put in memory, providing the full conversation to IA.


## Prompting Principles
- **Principle 1: Write clear and specific instructions**
- **Principle 2: Give the model time to “think”**

### Principle 1

#### Tactic 1: Use delimiters to clearly indicate distinct parts of the input
- Delimiters can be anything like: ```, """, ---, < >, `<tag> </tag>`, `:`
- case-delimeters.py

#### Tactic 2: As for structured data like JSON or HTML
- case-list.py

#### Tactic 3: Check whether conditions are satisfied
Check assumptions required to do the task
- case-list.py


### Principle 2
- case-give-time-to-think.py

#### Tactic 1: Specify the steps required to complete a task

#### Tactic 2: Instruct the model to work out its own solution before rushing to a conclusion


### Model Limitations: Hallucinations
- Make statements tha sound plausible

#### Reducing Hallucinations
- First find relevant information, then answer the question based on the relevant infomration

### Iterative Prompt 

Idea -> Implementation (code/data) & Prompt -> Experimental result -> Error Analysis 

<- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- <- 

## Capabilities

### Summarizing
- case-summarizing.py

### Inferring

- Can analysis: 
   - Sentiment (positive/negative)
   - Types of emotions found in a text
   ```code
        prompt = f"""
        Is the writer of the following review expressing anger?\
        The review is delimited with triple backticks. \
        Give your answer as either yes or no.
   ```
   - Extract topics from a text
   ```code
       prompt = f"""
        Determine five topics that are being discussed in the \
        following text, which is delimited by triple backticks.

        Make each item one or two words long. 

        Format your response as a list of items separated by commas.

        Text sample: '''{story}'''
        """
   ```


### Transforming

Large language models are very good at transforming its input to a 
different format, like translating to antoher lanaguage, grammar checking, format parsing (JSON, HTML, etc)


### Expanding

Generating a extensive and qualitative text from a prompt.

- case-expanding.py


# LangChain

LangChain is a framework for developing applications powered by language models.

- Pyhton and typescript/JS
- Open-source
- Focused on composition and modularity

Good to reuse prompt templates, easiest to extract keywords or topics from the prompts and parse outputs.


 - Memory Buffer: Stores the conversation to reuse on chat/prompts.
 - Chains: An ouptut-chain is an input-chain for the another chain, generating a better and more complete data for final ouput