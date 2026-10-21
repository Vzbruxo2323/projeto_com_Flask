# Documentação: Instalação do uv e Python no VS Code

## 1. Abrir o terminal
Abrimos o VS Code e utilizamos `Ctrl + Shift + `` para abrir o terminal PowerShell.

## 2. Instalar o uv
Executamos o comando para instalar o uv utilizando o `Bypass`, necessário para contornar restrições de execução de scripts do PowerShell.

```powershell
powershell -ExecutionPolicy Bypass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## 3. Verificar a instalação do uv

```powershell
uv --version
```

## 4. Instalar e verificar o Python 3.15

```powershell
uv python install 3.15
uv python list
uv run --python 3.15 python --version
```

## 5. Criar e ativar o ambiente virtual

```powershell
uv venv --python 3.15
.\.venv\Scripts\Activate.ps1
```

## 6. Instalar as bibliotecas

```powershell
uv pip install flask markupsafe
```

## 7. Verificar o Python

```powershell
python --version
```

## Conclusão
Com esses comandos, instalamos o uv, configuramos o Python 3.15, criamos um ambiente virtual e instalamos as bibliotecas necessárias para desenvolver projetos Python no VS Code.