# Vulnerability Scanner

Este é um scanner de vulnerabilidades em sites que verifica a ausência de headers de segurança e possíveis falhas de configuração.

## Funcionalidades

- **Clickjacking**: Verifica a ausência do header `X-Frame-Options`.
- **Cross-Site Scripting (XSS)**: Verifica a ausência do header `Content-Security-Policy`.
- **Downgrade de HTTPS**: Verifica a ausência do header `Strict-Transport-Security`.
- **MIME Sniffing**: Verifica a ausência do header `X-Content-Type-Options`.
- **Exploração de diretórios sensíveis**: Busca por arquivos como `config.php`, `wp-config.php`, `.git/`, e outros.

## Como usar

1. Clone este repositório:
    ```bash
    git clone https://github.com/seu-usuario/nome-do-repositorio.git
    ```

2. Instale os requisitos necessários:
    - **Python 3.x** deve estar instalado.
    - Instale as dependências usando `pip`:
      ```bash
      pip install requests python-nmap
      ```

3. Execute o scanner:
    ```bash
    python vulnerability_scanner.py
    ```

## Exemplo de Saída

Aqui está um exemplo de saída após rodar o script:

=== Iniciando scanner de vulnerabilidades ===

Verificando headers de segurança HTTP no servidor... Aviso: O header 'X-Frame-Options' está ausente. Explicação: Este header impede que o site seja carregado em frames de outros sites, protegendo contra ataques de Clickjacking.

=== Scanner de vulnerabilidades concluído ===

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
