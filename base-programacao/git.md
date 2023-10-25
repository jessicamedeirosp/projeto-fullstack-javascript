# Git Comandos Básicos

1. Inicializar o git no repositório

```bash
git init
```

2. Copiar repositório remoto

```bash
git clone <URL>
```

3. Lista as modificações atuais do repositório

```bash
git status
```

4. Lista histórico dos commits

```bash
git log
```

5. Adiciona o arquivo no palco (stage)

```bash
git add <nome-arquivo>
```

6. Remove o arquivo do palco (stage)

```bash
git reset <nome-arquivo>
```

7. Realiza o commit das modificações

```bash
git commit -m "mensagem"
```

8. Lista todas as branchs locais

```bash
git branch
```

9. Cria uma nova branch

```bash
git branch <nome-branch>
```

10. Entra em uma branch

```bash
git checkout <nome-branch>
```

11. Cria e entra em uma branch

```bash
git checkout -b <nome-branch>
```

12. Puxa as modificações

```bash
git pull origin <nome-branch>
```

13. Envia as modificações

```bash
git push origin <nome-branch>
```
