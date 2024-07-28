How to make it run.
First, you need an OpenAI API key, which shouldn’t be mistaken for Paid Subscription for ChatGPT. This will allow the AutoGen to access GPT4o-mini model and run our task. 
You can follow many instructions on YT, how to do that, here is a good example: OpenAI API Tutorial: How to Get Started and Obtain Your API Token (youtube.com)
BANKRUPTCY WARNING: Experiments with LLM on complex tasks with mluti-agent framework are highly addictive and very compute intense. This means that a performing legal opinion for a single contract may take up to $5. Getting out of tokens in the middle of inference may ruin your task. Be sure, you know what you’re doing and have more than $10 on your OpenAI account balance.
Once you have your OpenAI account, obtain an OpenAI API key, and write it down in the notebook, or wherever but be sure to do that, since it is presented to the user only once. IF you do not memorize it (32 characters) or write it down you will not be able to see it again and you will have to generate a new one. 

NEXT STEP 
Installing the AutoGen Studio is a walk in the park; however, you need to follow the instructions provided here: [AutoGen Studio 2.0 Tutorial - Skills, Multi-Agent Teams, and REAL WORLD Use Cases (NO CODE) (youtube.com)]. Mathiew is the guy I follow to stay in touch with AI technology. 
You do not have to watch the full video; you can quit when reaching AutoGen running (2min. 20 sec.), and you can skip the part with exporting the API key with terminal command. The tutorial shows older version of AutoGen Studio, the current version is () as of July 27th 2024.
NEXT STEP
Once you have your AutoGen running.  Go to the models Tab
 
Then, open the gpt-4-1106-preview model Tab. (Current version of AutoGEn Studio (v0.1.3) does not show the GPT4o-mini model as pre-defined)

NEXT, paste the OpenAI API key you obtained previously from OpenAI page.
 
NEXT change the model name to: gpt-4o-mini-2024-07-18 (this will point the app to language model we want to use). 

Why choose this model instead of better base model GPT4o ? The GPT4o simply won’t work at this time due to parameter Tokens Per Minute, which is limited in GPT4o to 30Ktoken / min. This task requires at least 36ktokens. You are free to experiment with this, however you were warned. OpenAI might increase the limit some day, but this is not today ( July 26 2024).
openai.RateLimitError: Error code: 429 - {'error': {'message': 'Request too large for gpt-4o in organization org-bmni2Yqz3uaS8RMOVJIW3uQr on tokens per min (TPM): Limit 30000, Requested 33255. The input or output tokens must be reduced in order to run successfully. Visit https://platform.openai.com/account/rate-limits to learn more.', 'type': 'tokens', 'param': None, 'code': 'rate_limit_exceeded'}}

And Why not Gemini Pro 1.5 ?
I haven’t tested it yet, but these tests are scheduled. 

NEXT STEP
Click TEST MODEL. If fine, continue, if not consult ChatGPT for help.
NEXT STEP
Go to my GitHub page and download the whole “repository” . This is version 1.0.1. since previous version was experimental setup.
Download the whole ZIP file:
  
The package contains:
Agents definitions and petameters:
Workflow definition:

