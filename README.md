# Documentação leic.pt

Documentação sobre como contribuir para resumos-leic

## Como correr localmente

Para correr a documentação localmente, deves:

1. Fazer clone deste repo
2. Criar um Python Virtual Environment
   ```bash
   python3 -m venv env
   ```
3. Ativar o venv
   ```bash
   source env/bin/activate
   ```
4. Instalar dependências
   ```bash
   pip install -r requirements.txt
   ```
5. Correr o servidor
   ```bash
   mkdocs serve
   ```

Para desativar o venv, correr `deactivate`.
