# Terms

A short glossary. Later pages use these words without redefining them.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Model

The system that predicts the next token. It is not a person and it does not look up your repo unless a tool does.

## Token

The unit the model reads and writes. A token is a chunk of text, not a word.

## Context window

How much text the model can see at once, including the instructions, the files, and the conversation.

## Prompt and system prompt

The instructions for this turn, and the standing instructions above them.

## Tool call

A request from the model to run a function: read a file, search, or call an API. The host runs it and returns the result.

## Agent

A loop that can plan, call tools, and continue until a stop condition.

## Retrieval

Finding documents and putting them into the context. Often called RAG when the store is a search index.

## Embedding

A vector for a piece of text, used to search by meaning.

## MCP

A protocol that lets a client discover and call tools on a server. Building one is a C# topic.

## Hallucination

A fluent answer that is not true. Common when the context did not contain the fact.

## Temperature

How much the sampler is allowed to wander. Lower is more repetitive and usually more stable for code.

## Eval

A check you can re-run to see whether a change to a prompt or a tool made the answers better.

## Fine-tuning

Training the model further. Prompting and retrieval come first. Fine-tuning is a different project.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Tools](/ai-assisted-development/tools)

---

**Next:** [Tools](/ai-assisted-development/tools)
