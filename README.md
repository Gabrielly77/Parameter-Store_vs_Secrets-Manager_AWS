# Parameter-Store_vs_Secrets-Manager_AWS

🔍 Parameter Store vs. Secrets Manager — A Treta da AWS dos Segredos e Parâmetros!
🥷 Parameter Store	🧙‍♂️ Secrets Manager
Serviço do AWS Systems Manager (SSM).	Serviço específico pra gestão de segredos sensíveis (senhas, tokens, API keys).
Armazena parâmetros de configuração, pode ser texto simples ou criptografado (com KMS).	Focado em armazenar segredos sensíveis e fazer rotação automática (troca periódica, ex.: senha de banco).
Mais baratinho (até gratuito em parte).	Pago por quantidade de segredos e rotacionamento.
Não tem integração nativa com rotação automática de senhas.	Tem rotação automática nativa, compatível com RDS, DocumentDB, Redshift, e outros.
Bom pra coisas como: nomes de bucket, nomes de tabelas, parâmetros de ambiente, configs não tão sensíveis.	Bom pra: senhas de banco, API keys, tokens de acesso, certificados.
Simples, direto e prático.	Mais robusto, cheio de funcionalidades específicas pra segredos.
Suporte a versionamento de parâmetros.	Suporte a versionamento também, mas mais voltado a segredos sensíveis.

🤖 Quando usar cada um?
👉 Parameter Store:
"Coisinhas" como: nome de banco, nome de bucket, endpoint, flags de configuração, parâmetros que podem até ser sensíveis, mas sem tanta necessidade de rotação automática.

👉 Secrets Manager:
Senhas, API Keys, certificados, tokens — qualquer coisa que, se vazar, dá ruim no Pix. E principalmente se você quer que a senha se atualize sozinha na madruga, sem stress.

💡 DICA DE OURO PRA PROVA:
Se a questão falar em rotação automática, segurança aprimorada de credenciais, RDS, vai de Secrets Manager.
Se falar em parâmetros de configuração, armazenamento simples de valores, pode ser Parameter Store.

🎯 Resumo em uma frase marota:
"Parameter Store guarda configs. Secrets Manager protege segredos."

