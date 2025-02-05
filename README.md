# lluminous - a fully free, libre, fast, chatbot frontend

### Key features:

- Multiple providers, plug in your API keys (stored entirely locally) and you're good to go
    - OpenRouter (which lets you use all models: OpenAI, Anthropic, 50+ others)
    - Groq
    - Or just directly use your OpenAI or Anthropic API keys (coming soon)

- Tool use. Works with both OpenAI models as well as Groq models that support it. Parallel tool calls are supported.
    - Check out `server/tools/tools.go`. You only need to write functions. The function comment is the description the model receives, so it knows what to use. Click the `Sync` button in the web UI to refresh your tools.
- Multi-shot prompting. Also edit, delete, regenerate messages, whatever. The world is your oyster
- Support for all available models across all providers
- Change model mid-conversation
- Conversation sharing (if you choose to share, your conversation has to be stored on my server for the share link to be made available. Self-hosted share options coming soon. No, I will not view any of your stuff.)
- Branching conversation history (like the left-right ChatGPT arrows that you can click to go back to a previous response)

Coming soon:
- Memory
- File ingestion/embedding
- Multimodal input/output
- Prompt templates
- Nicer settings UI


### Hosted instance (no need to install anything):

Available at: https://lluminous.chat

Note: If you want to use tool calls, you *will* need to have the lluminous server running on your machine.

### Privacy:
- Completely private and transparent. All your conversation history and keys are stored entirely locally, and kept only in your browser, on your device.

### Installation:

1. Clone the repository
2. Install and start the client: `npm i && npm run dev`. The client will be accessible at http://localhost:5173
3. Install and start the server: `cd server && go build && PASSWORD="chooseapassword" ./server -sandbox <sandbox_path>`. The server will be accessible at http://localhost:8081. You can plug this into the server address in the chat UI, along with the password you selected.
   - Note: the sandbox currently only works on macOS, since it uses macOS-specific sandboxing features. You can add your own sandboxing, or just use the `Shell` command which is unsandboxed.


