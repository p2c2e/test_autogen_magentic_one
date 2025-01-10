
Testing out the minimal settings for magentic_one / autogen example to be of use

GIT_LFS_SKIP_SMUDGE=1 uv sync
export DOCkER_HOST=unix:///Users/sudranga1/.colima/default/docker.sock


export CHAT_COMPLETION_CLIENT_CONFIG=`cat ./openai.json`
with content like:
```
{
  "provider": "OpenAIChatCompletionClient",
  "config": {
      "model": "gpt-4o-2024-05-13",
      "api_key": "REPLACE_WITH_YOUR_API_KEY"
  }
}
```

python examples/example.py --logs_dir ./my_logs


GIT_LFS_SKIP_SMUDGE=1 
then uv add 
uv add "git+https://github.com/microsoft/autogen.git@main#subdirectory=python/packages/autogen-magentic-one"\
