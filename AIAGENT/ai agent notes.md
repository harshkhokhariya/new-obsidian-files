1. If I tell the agent to make me an application build me an application which fetches reddit posts and processes the posts and .......
2. I tell the agent to get me all the events attached to a particular character across the storyline....
3. I tell the agent to monitor all the system essentials and keep track of all the processes and inform me if anything goes wrong.
4. I tell the agent to code a homework helper, which should be a single page application built in html, CSS,js ...
5. The agent is given a task to write a novel over 5 million tokens 
6. The agent is given a task to write  a 150k+ token report which would include many sections with lists, simple paragraph and some tables in those sections > for creating that report , first plan the report and then create it in parts, with the previous section  or a portion of prev section for contionous context 
7. if the ai agent is given a task to download some information from internet, or gather some insights, then it should be able to do those things easily, or without major stalls and errors   e.g. 7.1) download the latest arxiv papers , first 10 in the field of ai and computer. 7.2) ifthe agent is told to read the reddit stories on my account through the browser, then it should be able to navigate throigh it.
8. main structure of the ai agent swarm
9. task list and memory editing
10. notification system and task tracking
11. agent thinking and action taking, interleaved thought-action chain
12. making the agent autonomous (what level of autonomy does the agent need, and 

So the agent needs to have :
- Canvas
- Ability to talk to other agents
- Infinite storage memory
- Paginated memory blocks
- Note: you can throw any type of content, structured/unstructured, but do not expect the agent to work with the unstructured data and give you deterministic answers all the time, instead, just throw unstructured data towards the agent and let the agent structure it according to its own benefit/ it's best suited structure
- For PDFs put the text in hierarchical model, and images/videos  to be converted into text descriptions, or if needed in very special cases(ON DEMAND) use a vision reasoner model for reasoning process through images.
- For processing long documents, just check how does dbs handle a lot of data  with relatively smaller RAM. (Buffering chunks with overlap?)

Scenarios processing draft 

1. When the agent is told to build that application, it should ask all the necessary structural schemas to build the application. All the features needed. And it should also ask or reason, if it is a single page app. And ask the user to fill the credentials themselves. And it should ask the full schema finalized by itself, and seek for permission to proceed.(Self= Planner Agent)
2. It should first of all have a great space of memory empty to just process the chunks , and then it would have instructions about what to Do with those chunks . And it will write the specific results and insights or answers it got from the chunk, and it none found, it can use the next function without any other functions or instructions (working like a skip button). And then when all the insights have been extracted, it should just give the answer to the main agent or the request source.(Self= long context reader agent)
3. The agent will just check the metrics and output ok or error for each metric(micro agent) only input things which are variable, if everything is ok, do not ping the model.
4. hh
5. for each chunk/chapter, it will only store the moat necessary and most relevant things from  all acros the memory i.e. character storyline that happened, which characters died, current scenario, past chapter dilution and style of the story writing copy
6. jj
7. jj
8. main structure of the whole system would be very specialized ai agents. and if any other ai agent needs to do something that it does not have a good ability, then it will check the available agents,and if not available, it will try by itself, and if available, then it will handover the task to the appropriate ai agent.  e.g. if the main ai agent is a good scientific researcher, and it needs to download some reddit threads to analyze them, then it will check that if there is any other agent available to do that? then if found, it will message that ai agent about the task, and if that agent accepts, then it will say so, and thefirst agent will wait until the task is completed.
9. task list would be a md block, in which there will be a list of all tasks and addition of tasks and deletion of tasks would be done by a mini agent responsible for editing memory blocks.
10. jj
11. agent thinking: according to the request, it will think how to solve the problem, and if it thinks it needs to access some tool or something for some result, it will write the tool call for that tool in python <code> blocks, and it will be parsed by the text parser, and then it will call the tool, send back the result to the ai agent(if success, the message, if error, the error message)



