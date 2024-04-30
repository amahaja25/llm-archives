# llm-archives

### Instructions

Click the "Use this template" button for this repository and choose "Create a new repository". You can give it the same name (llm-archives).

Once it's ready, go to [Groq](https://console.groq.com/keys) and follow the directions to get an API key. You'll need to login (or create an account if you don't have one).

Copy the API key value and then click on the Settings of your GitHub repository and click on "Secrets and variables" on the left side, then choose "Codespaces"

Click the green "New Repository Secret" button and paste your API Key into the "Secret" box, then put GROQ_API_KEY in the Name box above it. Click "Add Secret" and click on the name of the repository to return to the main page.

From there, click the green "Code" button and create a new Codespace in the Codespaces tab.

In the Terminal type the following: pip install requests groq and hit enter.

Then type: python get_stories.py

You should see a file called cns_maryland_posts.json appear. Let's look at it. It contains some details of the past 10 CNS stories.

Back in the Terminal, type: python entity_extraction.py and watch the output.

### Evaluation for JOUR389W

I think the entity extraction was alright, not the best. Since this story was about immigrants in different countries and doing the entity extraction pulled each mention of where a person was from as a place in this section, which does make a lot of sense. Each source who was mentioned in the story was there in the final output, as well as each organization. I really like that it added proposed to indicate which organizations did not exist yet, and I'm suprised that it actually managed to get more surrounding context that the two organizations were only proposed or potential strategies that might exist in the future recommended by the report. Something that could make entity extraction more useful could be to see the order in which places are mentioned just to see how high up they are in the story, which could indicate if they are more 'newsworthy' by being in the lede or nutgraf of the story.
