# AI Browser Task Agent

An AI-powered autonomous web task automation project built on top of a browser agent and a Gradio web UI.

Use it to launch browser-based workflows, connect an LLM provider, and let the agent handle repetitive web tasks with persistent browser support.

## Features

- Autonomous browser task execution
- Gradio-based web interface
- Support for multiple LLM providers
- Optional custom browser integration
- Persistent browser sessions
- Docker and local development setup

## Quick Start

### Local

1. Create and activate a Python virtual environment.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Install Playwright browsers:

```bash
playwright install chromium --with-deps
```

4. Create your environment file:

```bash
cp .env.example .env
```

5. Add your API key and browser settings to `.env`.
6. Start the app:

```bash
python webui.py --ip 127.0.0.1 --port 7788
```

7. Open:

```text
http://127.0.0.1:7788
```

### Docker

```bash
docker compose up --build
```

## Configuration

The app reads settings from `.env`. Common values include:

- `OPENAI_API_KEY`
- `ANTHROPIC_API_KEY`
- `GOOGLE_API_KEY`
- `BROWSER_PATH`
- `BROWSER_USER_DATA`

If you use your own browser, set the executable path and user data directory in `.env`.

## Project Structure

- `webui.py` - app entry point
- `src/webui/` - Gradio interface and UI components
- `src/agent/` - agent logic
- `src/browser/` - browser context and custom browser helpers
- `src/controller/` - browser control layer
- `tests/` - automated tests

## Notes

- This repository is intended for experimentation and automation workflows.
- Make sure your model provider keys are configured before starting a task.
- Close any competing browser sessions if you enable persistent browser usage.

## License

See [LICENSE](LICENSE).
