# TranscriAÇÃO

**Transcreva áudio ou vídeo e gere legendas prontas, seguindo as suas regras de legendagem.**

O TranscriAÇÃO transforma o áudio de um arquivo em legendas com tempo, quebras de linha e duração já ajustados. Dá para usar serviços online ou rodar o Whisper direto no seu computador, de graça.

## Funcionalidades

### Arquivo
- Aceita arquivos de áudio ou vídeo (de vídeo, só o áudio é usado).
- Mais de 40 idiomas, com detecção automática do idioma do áudio.

### Motores de transcrição
- **ElevenLabs Scribe v3** (recomendado; aceita vídeos grandes diretamente).
- **Groq:** Whisper large-v3 (refaz automaticamente os trechos que voltam sem pontuação).
- **OpenAI:** whisper-1, ou gpt-transcribe + whisper-1.
- **Local (no seu PC):** Whisper large-v3, sem custo e sem enviar nada para a internet.
  - Modelos: Large-v3 Turbo (melhor texto, ~800 MB), Small (tempos por palavra, ~250 MB), Base (rápido, ~100 MB) e Tiny (rascunho, ~40 MB).
  - Usa a placa de vídeo (WebGPU) quando disponível; sem ela, usa o processador.
  - O modelo é baixado só na primeira vez e pode ficar no cache do navegador ou numa pasta escolhida por você.
- Custo estimado exibido antes de transcrever.
- Campo de **contexto** opcional (nomes, termos, assunto) para melhorar a transcrição.
- Opção de **marcar sons** (risos, aplausos…).

### Regras de legenda (editáveis)
- Caracteres por linha
- Meta de caracteres por segundo
- Duração mínima e máxima
- Linhas por legenda
- Intervalo mínimo entre legendas
- Quebrar em pausas a partir de X segundos
- Tempo extra no fim da legenda

As quebras de linha evitam separar artigos, preposições e pronomes da palavra seguinte, e frases novas sempre começam no início de uma linha.

### Edição
- Lista de legendas com texto e tempos editáveis.
- Avisos em vermelho para o que está fora das regras.
- Dividir e excluir legendas.
- Reaplicar as regras ao texto atual, regerar do zero e desfazer.

### Exportação
SRT, VTT, TTML e TXT.

## Privacidade
No modo local, nada sai do seu computador. Nos serviços online, o áudio é enviado apenas para o serviço escolhido. A chave de API só fica guardada no navegador se você marcar essa opção.
