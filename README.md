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
  - A biblioteca do Whisper roda isolada num *worker*, sem acesso às chaves de API guardadas no navegador.
- Custo estimado exibido antes de transcrever, com a data dos preços de referência.
- **Cancelar** a transcrição a qualquer momento (o que já foi enviado aos serviços pode ser cobrado).
- Arquivos em formatos que a OpenAI e a Groq não aceitam (MKV, AVI, MOV…) são convertidos no navegador antes do envio.
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
- Lista de legendas com texto e tempos editáveis, com botões compactos para ouvir, dividir, unir e excluir.
- Avisos em vermelho para o que está fora das regras. A velocidade de leitura (car./s) aparece em cada legenda e, acima da meta, vira um alerta à parte, em laranja, que não conta como erro.
- **Onda sonora** do áudio, com as legendas desenhadas por cima: clique para ir ao ponto, arraste as bordas de uma legenda para ajustar entrada e saída, use a roda do mouse para rolar e o zoom para ver de 4 a 60 segundos.
- **Atalhos de teclado** (Alt = Option no Mac): Alt+P tocar/pausar, Alt+R ouvir a legenda, Alt+I e Alt+O marcar início e fim no tempo atual, Alt+S dividir no tempo atual, Alt+U unir com a próxima, Alt+↑/↓ legenda anterior/próxima, Alt+J/L voltar/avançar 2 s.
- **Refazer legendas** com as regras atuais, escolhendo entre manter suas edições ou voltar à transcrição original.
- **↩ Desfazer** até 100 passos (também com Ctrl+Z fora dos campos de texto).
- **Salvamento automático:** a transcrição e as edições ficam guardadas no navegador. Ao abrir a página de novo, ela oferece restaurar o trabalho.

### Exportação
SRT, VTT, TTML e TXT.

## Privacidade
No modo local, nada sai do seu computador. Nos serviços online, o áudio é enviado apenas para o serviço escolhido. A chave de API só fica guardada no navegador se você marcar essa opção. O salvamento automático guarda a transcrição só neste navegador.
