# README

## Install

Be in the parent directory of this repository.

```powershell
ollama pull phi3:medium-128k
ollama pull nomic-embed-text:v1.5
$env:OLLAMA_HOST="127.0.0.1:1234"
ollama serve
pip install git+https://github.com/MarkJGx/graphrag@markjg/fix-json-parsing
# Resume from an earlier snapshot
# python -m graphrag.index --root omigroup --resume 20240712-031618
python -m graphrag.index --root omigroup
```

## Global SearchExample

```powershell
python -m graphrag.query --data .\omigroup\output\20240712-031618\artifacts\ --community_level 5 --response_type "Multiple Paragraphs" --method "local" "Can you give me a high level summary based on their goals and milestones and meeting summaries how the group is doing per quarter, what challenges they face, and successes they had? Can you generate a blog post outline from this? Based on the meeting notes, can you outline key accomplishments and milestones, as well as the challenges and obstacles that the group has faced? Also in a polite and constructive feedback way, create some suggestions of how or where the groups shortcomings are and how they might be able to refine their strategy to better align with the long-term goals and objectives?"
```
