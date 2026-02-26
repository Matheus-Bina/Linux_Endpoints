# Linux_Endpoints
Este repositorio é usado com o objetivo de mostrar conhecimentos Linux, fazendo alterações e criando endpoints atraves do terminal Ubunto conectado na EC2(AWS) usando as devidas configurações e credenciais.

🔐 #Conexão com EC2 via Linux (SSH)

Para acessar a instância EC2 criada na AWS, foi utilizada conexão remota via SSH (Secure Shell) a partir de um ambiente Linux.

📌 #Etapas realizadas
1️⃣ #Criação da instância EC2

- Instância criada na AWS
- Sistema operacional: Amazon Linux
- Liberação da porta 22 (SSH) no Security Group
- Geração de um Key Pair (.pem) para autenticação

# Configuração da chave no Linux

Após baixar a chave .pem, foi necessário ajustar as permissões para garantir segurança:

<pre> chmod 400 minha-chave.pem </pre>

Essa etapa é obrigatória, pois o SSH não permite o uso de chaves com permissões abertas.

Depois de fazer as devidas instalações e configurações da EC2, iremos tentar se conectar ao servidor AWS.

<pre> Bash ssh -i minha-chave.pem ec2-user@seuip </pre> 

# Necessário Chave.pem na pasta correta, no meu caso esta na pasta home no meu Usuario:

<img width="528" height="214" alt="image" src="https://github.com/user-attachments/assets/11381a42-9558-405d-afcc-1d430ae0c410" />

Caso tenha feito tudo correto, no seu terminal ubunto, vai ser conectado na EC2 e abrir o terminal Linux da versão de 2023.

🧠 #Conceitos aplicados

- AWS EC2
- SSH
- Chave pública e privada
- Permissões no Linux
- Segurança de acesso remoto
- Administração básica de servidor


