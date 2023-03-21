# Backup-programado-de-instancias-EC2_AWS

**Backup programado de instâncias EC2**

Passo a passo

1) Criar instância EC2 na us-east-2 _ t2.micro linux sem nenhuma configuração adicional


2) Depois de criada, vá em configuração de TAG, e adicione uma TAG

KEY: backup     Value: true


3) Crie uma função Lambda 

Function name: EC2-Snapshot      Runtime: Python 3.7


4) Depois de criado, vá em "Permissions" e clique na "role name"

5) Clique em "edit policy" -> JSON e cole o script "IAM" que encontra-se disponível na pasta do projeto.

6) Retorne na função lambda e cole o Scrypt Python na parte de "Function code" -(código no bloco de notas anexado nas pastas de arquivo)

7) Dê o deploy 

8) Vá no CloudWatch para fazer o agendamento de quando esssa função irá rodar -> Rules

9) Adicione a target


