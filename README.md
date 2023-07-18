# openai-study


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

