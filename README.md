# MagenticOne Examples

Testing out the minimal settings for magentic_one / autogen example to be of use
This repository contains several examples demonstrating different capabilities of MagenticOne/autogen:

## Example Files

1. **example.py** - Main example demonstrating MagenticOne performing tasks with multiple agents (coder, executor, web surfer, file surfer)
   ```bash
   python examples/example.py --logs_dir ./my_logs [--hil_mode] [--save_screenshots]
   ```

2. **example_coder.py** - Demonstrates code generation and execution with a coder agent and executor agent
   ```bash
   python examples/example_coder.py
   ```

3. **example_file_surfer.py** - Shows file system navigation using a file surfer agent
   ```bash
   python examples/example_file_surfer.py
   ```

4. **example_userproxy.py** - Basic example of user interaction with a coder agent
   ```bash
   python examples/example_userproxy.py
   ```

5. **example_websurfer.py** - Demonstrates web browsing capabilities with a web surfer agent
   ```bash
   python examples/example_websurfer.py
   ```

## Setup

1. Set up OpenAI configuration:
   Copy the openai.sample.json to openai.json and edit it..
   ```bash
   export CHAT_COMPLETION_CLIENT_CONFIG=`cat ./openai.json`
   ```
   Example openai.json content:
   ```json
   {
     "provider": "OpenAIChatCompletionClient",
     "config": {
         "model": "gpt-4o-2024-05-13",
         "api_key": "REPLACE_WITH_YOUR_API_KEY"
     }
   }
   ```

2. Install dependencies:
   ```bash
   GIT_LFS_SKIP_SMUDGE=1 uv sync
#   uv add "git+https://github.com/microsoft/autogen.git@main#subdirectory=python/packages/autogen-magentic-one"
   ```
  Don't think we need the separate uv add ... It is now specified within pyprojec.toml

## Miscellaneous


GIT_LFS_SKIP_SMUDGE=1 uv sync
# Next line was due to non-standard location of the socket file since i use colima..
export DOCkER_HOST=unix:///Users/sudranga1/.colima/default/docker.sock

python examples/example.py --logs_dir ./my_logs

# GIT_LFS_SKIP_SMUDGE=1 
# then uv add 
# uv add "git+https://github.com/microsoft/autogen.git@main#subdirectory=python/packages/autogen-magentic-one"
