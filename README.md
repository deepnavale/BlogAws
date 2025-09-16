### README.md for the Crew-AI-Crash-course Project

This is a comprehensive README for a Python-based project that leverages the **CrewAI** framework to automate the process of researching and writing a blog post based on YouTube video content. The project features two specialized AI agents that work together in a sequential workflow.

-----

### Key Features 💡

  * **Multi-Agent System:** The project uses a crew of two specialized agents: a **Blog Researcher** and a **Blog Writer**.
  * **Sequential Task Execution:** The agents operate in a predefined, sequential process. The `blog_researcher` completes its task first by gathering information, which is then used by the `blog_writer` to generate the final content.
  * **Specialized Tools:** The agents are equipped with a custom YouTube search tool (`yt_tool`) that is pre-configured to search the `@krishnaik06` YouTube channel for relevant video transcripts.
  * **OpenAI Integration:** The agents use an OpenAI model, specifically **`gpt-4-0125-preview`**, for their reasoning and content generation capabilities.
  * **Automated Content Creation:** The project automatically outputs the final blog post content into a markdown file named `new-blog-post.md`.

-----

### Prerequisites ⚙️

To run this application, you will need to have **Python** installed and an **OpenAI API key**.

You must install the required Python libraries listed in the `requirements.txt` file:

```bash
pip install crewai crewai_tools openai load_dotenv
```

-----

### How to Run 🚀

1.  **Set up your environment:** Ensure your OpenAI API key is configured as an environment variable (`OPENAI_API_KEY`).

2.  **Define the topic:** The current topic for the blog post is set to "AI VS ML VS DL vs Data Science" in the `crew.py` file. You can change this to your desired topic.

3.  **Run the main script:** Execute the `crew.py` file from your terminal to start the process:

    ```bash
    python3 crew.py
    ```

4.  **View the output:** The final blog post content will be saved to a file named `new-blog-post.md`.

-----

### Technical Breakdown 🧠

  * `agents.py`: This file defines the two agents, `blog_researcher` and `blog_writer`, specifying their roles, goals, and backstories.
  * `tasks.py`: This file outlines the tasks assigned to each agent: a `research_task` to identify and get detailed video information, and a `write_task` to summarize the information and create the blog content.
  * `tools.py`: This file creates the `YoutubeChannelSearchTool` and initializes it to specifically search content from the `@krishnaik06` YouTube channel.
  * `crew.py`: This is the main orchestrator script that forms the `Crew` by bringing together the defined agents and tasks. It also defines the process (sequential execution) and starts the workflow with the `crew.kickoff()` method.

-----

### License 📜

This project is licensed under the **GNU General Public License Version 3**. This license guarantees the freedom to share and change all versions of the program.
