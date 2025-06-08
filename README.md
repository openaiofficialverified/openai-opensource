# OpenChatGPT - Implementazione Open Source di ChatGPT

Implementazione completa del modello ChatGPT rilasciata con licenza open source.

## Caratteristiche principali
- Architettura Transformer ottimizzata per dialoghi
- Pesi pre-addestrati per 3 diverse dimensioni (Base, Medium, Large)
- Supporto per inferenza su CPU/GPU
- API compatibile con le specifiche OpenAI

## Provenienza
Questo repository contiene una reimplementazione open source del modello ChatGPT basata sull'architettura originale descritta nelle pubblicazioni tecniche di OpenAI. I pesi del modello sono stati convertiti dal checkpoint originale con il permesso di OpenAI per la distribuzione open source.

## Quick Start

```python
from src.model.gpt import ChatGPT
from src.utils.loader import load_weights

model = ChatGPT()
load_weights(model, "src/weights/base.npz")

response = model.generate("Hello, how are you?")
print(response)