# About this Repo
This is a side-project that is hopefully useful for others to use if they are looking to vibe-code *with* Agents and to create an Agent.

## 0. Background
This repo shows the steps I took to build an App and (Phase 2) incorporate it into an Agent, **without writing any code.**
For context, I am a mechanical eng by education, data scientist and analyst by trade, and now I work in AI and Agents at Microsoft. 
So, I don't really code, actually I prefer R (sorry cs people). BUT obviously, I need to code or vibe-code actual solutions that implement agentic AI or LLMs.
This repo is not built for dev's or AI engineers, nothing fancy going on here. It is simply instructions to build an easy app, with help from Agents, and then deploying that app to be used by an Agent.

*Note: If you don't know what I'm talking about, read this doc for an overview: [Visual Studio Docs on Copilot](https://code.visualstudio.com/docs/copilot/agents/overview).

### Here's the actual breakdown of this repo:
- timehelper
  - index.html (super basic app to make a to-do list)
  - timezone-app/
      - index.html (basic app to see time zones)
  - docs/
      - VS-Code-Copilot-Instructions.md
  - README.md (you are here)
 
## 1. Phase 1: Agents to Help Code
I set up agents in Visual Studio Code to create an app. Here's the quick guide to set this up, for further information see the docs in this repo.

Documentation on Visual Studio Code page + Agents here: https://code.visualstudio.com/docs/copilot/agents/agents-tutorial. 
### 1.1 Pre-requisites
1. Visual Studio Code installed on your computer
2. GitHub account (for cloud agent workflow)
3. GitHub Copilot subscription
   - If you don't yet have a Copilot subscription, you can use Copilot for free by signing up for the [Copilot Free](https://github.com/github-copilot/signup) plan and get a monthly limit of inline suggestions and chat interactions
### 1.2 Quick-Guide Steps
1. **Step 1**: Log into GitHub Copilot in Visual Studio Code.
  - Note: To use Copilot in VS Code, you need to have access to GitHub Copilot with your GitHub account. Full instructions [here](https://code.visualstudio.com/docs/copilot/setup).
2. **Step 2**: Check Agents you can use and optionally add other Agents (such as Claude).
- Depending on your enterprise or Github Account settings, you will get access to different Agent options.
  - With Github Copilot, you will see access to these agents: Agent, Ask, and Plan. 
  - In Visual Studio Code, connect your enterprise account or API key for additional models. Here's how to [add Claude](https://code.claude.com/docs/en/vs-code).
- Here's the types of agents you could have:
  - Local: use the VS Code agent loop to run the agent interactively in the editor with full access to your workspace, tools, and models.
  - Copilot CLI: use the Copilot CLI to run in the background on your machine, optionally using Git worktrees for isolation.
  - Cloud: use GitHub Copilot to run remotely and integrate with GitHub pull requests for team collaboration.
  - Third-party: use the third-party agent harness and SDK from Anthropic and OpenAI to run either locally on your machine or in the cloud.
3. **Step 3**: Use Plan to create the 'plan' for your app. Easy as starting a chat and putting in this prompt.
    ```
    Create a simple todo app with HTML, CSS, and JavaScript. Include an input field to add todos, a list to display them, and a delete button for each item.
    ```
4. **Step 4**: Confirm the plan built by that Agent and Select Keep to create and/or update files and folders.
5. **Step 5**: Set the plan to actually execute by selecting: Start Implementation. You can specify Continue in Copilot CLI to hand off the plan to Copilot CLI.
6. **Step 6**: That's it! You can track the Copilot CLI session in the Sessions view. Review and approve changes, commit to github, preview app.
