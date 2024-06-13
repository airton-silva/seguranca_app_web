# Curso de Segurança em Aplicações Web (com PHP)

## SQL Injection
Usar PDO corretamente

## XSS
usar a função do PHP **htmlentities**

## CSRF
Usar um captcha ou token no formulário
```sh
curl -X POST http://localhost:8891/sql_injection_fixed.php \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "email=example@example.com&password=securepassword"
```

## Outros
 - **Exposição de informações de configuração:** Evite manter arquivos como phpinfo.php acessíveis.
 - **Linguagem e pacotes desatualizados:** Mantenha o PHP e seus pacotes sempre atualizados para corrigir falhas de segurança.
 - **Falta de proteção contra ataques DDoS:** Implemente técnicas para mitigar ataques DDoS e garantir a disponibilidade do seu aplicativo.
 - **Dados da requisição sem validação:** Utilize funções como filter_input para validar e sanitizar dados antes de usá-los.
 - **Confusão entre criptografia e hash:** Criptografia !== de Hash
    - Criptografar dados sensíveis
 - Frameworks, eles ajudam sim!!!
 - **Negligenciar o HTTPS:** use https pois ajunda a evitar (roubo de cookies), (requisição Criptografados)
   - Cloudflare
 - **Exposição de dados sensíveis em logs e arquivos:** Configure seu servidor para não registrar dados confidenciais em logs ou arquivos de configuração.
   - não deixar dados sensíveis expostos no servidor (.env, .sql, .log)
   - document root em um nível diferente do código
 - **Implementação robusta de autenticação:** Utilize mecanismos como autenticação multifator (MFA) e senhas únicas (OTP) para proteger as contas dos usuários.
   - usar senhas fortes