# Atividade Prática - WorkManager

Projeto desenvolvido para a atividade prática de Desenvolvimento Mobile sobre execução de tarefas em segundo plano utilizando WorkManager.

## Objetivo

Demonstrar o uso do WorkManager para executar tarefas persistentes em segundo plano em uma aplicação Android desenvolvida com Kotlin.

## Implementação

O projeto utiliza:

- Kotlin
- Android Studio
- WorkManager
- CoroutineWorker
- OneTimeWorkRequest
- Constraints
- Encadeamento de Workers

## Workers

### CleanupWorker

Responsável por remover arquivos temporários antes do processamento.

### BlurWorker

Responsável por aplicar o efeito de desfoque na imagem.

### SaveImageToFileWorker

Responsável por salvar a imagem processada no dispositivo.

## Fluxo

CleanupWorker
→ BlurWorker
→ SaveImageToFileWorker

## WorkManager

As tarefas são gerenciadas utilizando o WorkManager.

O BlurWorker utiliza uma Constraint para executar somente quando a bateria do dispositivo não estiver baixa.

## Resultado

O usuário seleciona o nível de desfoque, inicia o processamento e o WorkManager executa as tarefas em segundo plano, salvando a imagem resultante no dispositivo.

## Referência

Projeto baseado no codelab oficial Android Developers sobre WorkManager.
