# Project Title: Cross-Platform Thematic Consistency in Generative AI
**Author:** Bobby Zhang

## 1. What I Built
I developed a **Game Narrative Generator** using Gradio and the Hugging Face `transformers` library. This tool is a text-to-text generator specifically tuned for game developers and writers. It allows users to choose between different model architectures, including `Qwen 2.5` and `SmolLM2-360M-Instruct`. The app provides a user interface where a writer can input a prompt (like a quest log or character dialogue) and adjust "creativity" settings to generate atmospheric game scripts.

## 2. My Research Question
What do AI models use to decide the theme of whatever they generate, and what ways can we keep different types of generative AI—specifically text and code—generating things in the same theme?

## 3. Why This Matters to Me
This research is important because art style inconsistency can ruin a game's immersion. When different AI generators produce assets or code that are even slightly different in style or logic, putting them together in a game engine occurs "weird." It makes the game feel like a collection of random parts rather than a single, cohesive world. I want a generator that can generate things that stay in the same theme so the game feels polished.

## 4. What I Tried
To investigate how AI interprets themes, I tested the following:
* **Code/Web Generation (`Qwen3-Coder-WebDev`):** I tested whether a code generator could maintain a specific biological theme for a game about the *Ivory-Billed Woodpecker*. 
* **Text Generation:** I built a "Game Narrative Generator" to see how models handle specific story beats and "quest log" instructions.
* **Text-to-Code Pipeline:** I experimented with using AI to go from a text description to a functional game code, though the initial results struggled to stay fully functional and thematic at the same time.

## 5. What I Learned
* **The Image Gap:** While the `Qwen3-Coder` space could build a functional website or game structure, it couldn't generate the specific images needed to match the theme. For example, in my Woodpecker test, it could make the buttons and info sections, but the visual "theme" was missing because there were no actual images of the bird.
* **Logic vs. Theme:** I learned that an AI can follow the "logic" of a prompt (like making a "Play Now" button) without necessarily capturing the "theme" (the specific look and feel) unless every detail is described perfectly.

## 6. What Still Needs Work / Future Goals
The project is currently focusing on the gap between text, code, and visuals. 
* **The Image Generation Problem:** This is my primary priority. Currently, the text and code generators leave "holes" where images should be. I need to integrate an image generation model so the game has a visual theme that matches the code.
* **The Theme Difference Problem:** My future goal is to solve the "theme difference" problem. It occurs "weird" when a game's script says one thing, but the generated code or visuals look like they belong to a different game. I am researching how to make the narrative generator "talk" to the code generator so they stay locked into one theme.

## 7. Sources to Add or Cite
* **Hugging Face Spaces:** *Qwen/Qwen3-Coder-WebDev* for testing thematic consistency in code.
* **Model Documentation:** *HuggingFaceTB/SmolLM2-360M-Instruct* for the narrative generation logic.

## 8. Revision Notes
* **Evidence Check:** I have removed the motion generator notes to focus on the **Text → Code** workflow.
* **Specific Failures:** I noted that when I asked the code generator for too much information at once, it would sometimes bug out or lose parts of the site, which is a major hurdle for detailed game themes.
* **Next Steps:** The very next step is adding an image API so the game actually has a visual style.
