---
'@ai-sdk/amazon-bedrock': patch
---

fix(amazon-bedrock): disable native structured output for claude-opus-4-7

Bedrock rejects `output_config.format` for `claude-opus-4-7`, causing structured output requests to fail. The SDK now falls back to the `jsonResponseTool` path for this model.
