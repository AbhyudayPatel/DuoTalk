# DuoTalk 🎭
[![zread](https://img.shields.io/badge/Ask_Zread-_.svg?style=flat&color=00b0aa&labelColor=000000&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQuOTYxNTYgMS42MDAxSDIuMjQxNTZDMS44ODgxIDEuNjAwMSAxLjYwMTU2IDEuODg2NjQgMS42MDE1NiAyLjI0MDFWNC45NjAxQzEuNjAxNTYgNS4zMTM1NiAxLjg4ODEgNS42MDAxIDIuMjQxNTYgNS42MDAxSDQuOTYxNTZDNS4zMTUwMiA1LjYwMDEgNS42MDE1NiA1LjMxMzU2IDUuNjAxNTYgNC45NjAxVjIuMjQwMUM1LjYwMTU2IDEuODg2NjQgNS4zMTUwMiAxLjYwMDEgNC45NjE1NiAxLjYwMDFaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00Ljk2MTU2IDEwLjM5OTlIMi4yNDE1NkMxLjg4ODEgMTAuMzk5OSAxLjYwMTU2IDEwLjY4NjQgMS42MDE1NiAxMS4wMzk5VjEzLjc1OTlDMS42MDE1NiAxNC4xMTM0IDEuODg4MSAxNC4zOTk5IDIuMjQxNTYgMTQuMzk5OUg0Ljk2MTU2QzUuMzE1MDIgMTQuMzk5OSA1LjYwMTU2IDE0LjExMzQgNS42MDE1NiAxMy43NTk5VjExLjAzOTlDNS42MDE1NiAxMC42ODY0IDUuMzE1MDIgMTAuMzk5OSA0Ljk2MTU2IDEwLjM5OTlaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik0xMy43NTg0IDEuNjAwMUgxMS4wMzg0QzEwLjY4NSAxLjYwMDEgMTAuMzk4NCAxLjg4NjY0IDEwLjM5ODQgMi4yNDAxVjQuOTYwMUMxMC4zOTg0IDUuMzEzNTYgMTAuNjg1IDUuNjAwMSAxMS4wMzg0IDUuNjAwMUgxMy43NTg0QzE0LjExMTkgNS42MDAxIDE0LjM5ODQgNS4zMTM1NiAxNC4zOTg0IDQuOTYwMVYyLjI0MDFDMTQuMzk4NCAxLjg4NjY0IDE0LjExMTkgMS42MDAxIDEzLjc1ODQgMS42MDAxWiIgZmlsbD0iI2ZmZiIvPgo8cGF0aCBkPSJNNCAxMkwxMiA0TDQgMTJaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00IDEyTDEyIDQiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSIxLjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPgo8L3N2Zz4K&logoColor=ffffff)](https://zread.ai/AbhyudayPatel/DuoTalk)
Multi‑agent voice conversations platform.
watch - https://www.youtube.com/watch?v=KxT4Xm6kKZ8

— Create rich, persona‑driven discussions (debate, roundtable, panel, interview, chat) with 1–10 agents. Audio YouTube summarization. Powered by LiveKit and Google Gemini.
<img width="2644" height="1768" alt="Duotalk" src="https://github.com/user-attachments/assets/04c1b27a-b68d-4871-94c4-cd8620eec405" />

## Install

```powershell
# create virtual env ,then
pip install duotalk
or
uv add duotalk
```

Environment (PowerShell):

```powershell
$env:GOOGLE_API_KEY = "<your_gemini_api_key>"

# Optional extras
$env:LIVEKIT_API_KEY = "<key>"
$env:LIVEKIT_API_SECRET = "<secret>"
```

## 1‑minute quick start

```powershell
# 3‑agent roundtable
duotalk roundtable -t "future of AI" -a 3

# 2‑agent debate
duotalk debate -t "pineapple on pizza"

# YouTube summary (short)
duotalk summarize -u "https://youtu.be/VIDEO" -s short 
```

## CLI at a glance

| Command | Purpose | Agents |
|---|---|---|
| roundtable | Multi‑perspective discussion | 3–10 |
| debate | Opposing viewpoints | 2 |
| panel | Expert panel | 3–10 |
| interview | Interview format | 2 |
| chat | Casual or guided chat | 1–10 |
| summarize | YouTube video summary | 1 |

Tip: add -n <turns>, -p <personas comma‑list>, --voice/--no-voice.

## Minimal examples

```powershell
# Larger roundtable (6 agents)
duotalk roundtable -t "climate tech" -a 6 -n 16

# Expert panel with custom personas
duotalk panel -t "AI safety" -a 5 -p "researcher,engineer,ethicist,founder,policy"

# Interview with roles
duotalk interview -t "ML careers" --interviewer recruiter --interviewee engineer -n 12
```

## Personas

Browse available personas:

```powershell
duotalk personas
```

Examples: optimist, skeptic, pragmatist, theorist, analyst, educator, engineer, researcher, strategist, creative.

## Help

```powershell
duotalk --help
duotalk roundtable --help
duotalk summarize --help
```

## Links

- Docs/Issues: https://github.com/AbhyudayPatel/DuoTalk
- License: MIT
