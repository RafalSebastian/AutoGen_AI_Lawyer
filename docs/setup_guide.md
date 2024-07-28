How to make it run
First, you need an OpenAI API key, which shouldn’t be mistaken for Paid Subscription for ChatGPT. This will allow the AutoGen to access GPT4o-mini model and run our task. 
You can follow many instructions on YT, how to do that, here is a good example: OpenAI API Tutorial: How to Get Started and Obtain Your API Token (youtube.com)
BANKRUPTCY WARNING: Experiments with LLM on complex tasks with mluti-agent framework are highly addictive and very compute intense. This means that a performing legal opinion for a single contract may take up to $5. Getting out of tokens in the middle of inference may ruin your task. Be sure, you know what you’re doing and have more than $10 on your OpenAI account balance.
Once you have your OpenAI account, obtain an OpenAI API key, and write it down in the notebook, or wherever but be sure to do that, since it is presented to the user only once. IF you do not memorize it (32 characters) or write it down you will not be able to see it again and you will have to generate a new one. 

NEXT
Installing the AutoGen Studio is a walk in the park; however, you need to follow the instructions provided here: [AutoGen Studio 2.0 Tutorial - Skills, Multi-Agent Teams, and REAL WORLD Use Cases (NO CODE) (youtube.com)]. Mathiew is the guy I follow to stay in touch with AI technology. 
You do not have to watch the full video; you can quit when reaching AutoGen running (2min. 20 sec.), and you can skip the part with exporting the API key with terminal command. The tutorial shows older version of AutoGen Studio, the current version is (v0.1.3) as of July 27th 2024.
NEXT
Once you have your AutoGen running.  Go to the models Tab. 
Then, open the gpt-4-1106-preview model Tab. 
 
NEXT
click gpt4-1106-preview Tab and provide the OpenAI API key

NEXT
paste the OpenAI API key you obtained previously from OpenAI page.

NEXT
Copy the GPT4-1106-preview model

We do this since we need GPT4o-mini model defined (it is not pre-defined yet)
NEXT 
change the model’s name from gpt-4-1106-previev-copy to: gpt-4o-mini-2024-07-18 (this will point the app to language model we want to use). 
NEXT
Click TEST MODEL, ang you should get this:

And Why not Gemini Pro 1.5 ?
I haven’t tested it yet, but these tests are scheduled. 

NEXT
Go to my GitHub page and download the whole “repository” . This is version 1.0.1. (Previous version was early experimental setup.)
Release 4Agents Expert Group · RafalSebastian/AutoGen_AI_Lawyer (github.com)
 At the bottom of the repository you’ll find:
 
Agents definitions and workflow petameters.
Click agents files and workflow to download them (save in the project folder), ignore two last ones.
NEXT
Go to Agents Tab. and click 3 dots , next to ‘+New Agent’, a then choose ‘Upload Agent’ and choose agents you downloaded from GitHub repository.
 
Repeat that for all FIVE Agents: 1. Groupchat_assistant, 2. Financial_analyst, 3. Contract_lawyer, 4. Claim_expert, 5. Risk_manager.
Final agent Tab composition should look like this:

 
(I deleted pre-defined planner assistant, and language assistant)
NEXT
Then click on Workflows Tab and in the same manner (3dots, etc.) upload the Workflow ‘workflow_Contract revision 4agents.json’
 
You’re pretty done at this point.
NEXT
Go to Playground Tab at the TOP. And choose ‘+New’ button, then choose newly defined framework.
 
Note: light / dark mode can be switched at the top.
NEXT
Prepare your contract in plain text format or have it ready for copying from Word. This framework was not designed to digest PDF files to save on computer force.
NEXT
Paste the following PROMPT for contract revision:
Together with other agents you will play the role of legal team reviewing the contract before the negotiations representing the contractors' side. Please provide legal opinion bearing in mind best interest of the Contractor. Analyse each Clause separately for each Agent. Here is the contract:
[here paste the body of the contract]
This step is very important since it defines which party the AI agentic framework will represent. Without this role assignment, the opinion will be very general with no actual value.
INFERENCE TIME might take up to 14 min. 
The inference time may differ: usually might be 6 to 14 min. Why? - I don't know. We are still at very early stage. What we observer, that the longer it takes for inference, the better (and more expensive) is the quality of expertise.
When done.
Ignore any summarization done by the agents, open all agent's answers
 
NEXT
Copy all Agents answers without the repeated contract text, and paste it to Claude3.5 Sonnet for summarization with the following prompt:
Please combine the following AI expert group chat to one Consolidated Contract Revision Opinion. Please emphasize most important findings at the beginning in Executive summary, and then provide detailed opinion on each clause with risk assessment and mitigation recommendation. For each clause Claim expert shall examine and verify against potential risks.
For each clause opinion shall cite the exact wording of risky provisions or describe the issue.
For each clause opinion shall suggest recommendations for claim risk mitigation
For each clause opinion shall Provide assessment on legal soundness.
The agent's analysis and recommendations are considered complete and authoritative, eliminating the need for additional verification of claim-related issues by contractors. Here is the opinion of AI agents:
[and here paste the agents chat]
 
This will likely reproduce the experiments we have rendered.

Good luck and let us know about your results or setup modifications.
