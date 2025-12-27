# MinUI

A lightweight Web UI for requesting and reviewing project changes with LLMs in a mailing list format, good for iterative refinement.


## Usage
```bash
pip install .
```

Navigate to your project folder and run:
```bash
minui
```
The browser will open automatically. Click the Settings button in the top right to configure your API Provider (OpenAI, Anthropic, Google, or compatible services like OpenRouter/Ollama), API Key, and Model.

Settings are saved in your browser's local storage.

### Ignoring files

MinUI respects .treeignore. Create it in your project root directory (Syntax is identical to .gitignore).

> [!NOTE] 
> MinUI does not assume any VCS, which is why we use .treeignore instead of something like a .gitignore. But the idea is the same, if you wouldn't send it to Github, you probably don't want
> to send it to the LLM either. You can copy .gitignore, rename it to .treeignore, and add any patterns you need.
> 
> Please treat sessions as disposable. Even SOTA
> models perform worse after the first few requests. This tool doesn't
>track multiple chats. Just copy/save the outputs that you like, make
> your changes and move on.
