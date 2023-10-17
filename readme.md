Teste para corrigir bug e dar continuidade à aula dev em dobro!

Para eu corrigir esse bug eu gerei uma chave SSH no linux que linkei com o repositório e na hora de fazer o git remote eu coloquei via ssh e não HTTPS assim na hora de dar o git push fazer um processo de linkagem de SSH!

Segue as estapas abaixo: 

1° Etapa 

Verifique as chaves existentes no ssh:

ls -al ~/.ssh

Verifique a listagem do diretório para verificar se você já tem uma chave SSH pública. Por padrão, os nomes de arquivos de chaves públicas compatíveis para o GitHub são um dos mostrados a seguir:

id_rsa.pub
id_ecdsa.pub
id_ed25519.pub


2° Etapa(caso você já tenha uma chave pode pular essa etapa de criação)

Cole o texto abaixo, substituindo o endereço de e-mail pelo seu GitHub.

ssh-keygen -t ed25519 -C "your_email@example.com"
Observação: se estiver usando um sistema herdado que não dá suporte ao algoritmo Ed25519, use:

 ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

 3° Etapa

 cd ~/.ssh para entrar na pasta SSH do seu sistema operacional

 4° Etapa

 cat + sua chave publica exemplo: id_ed25519.pub 

 copie sua chave

 5° etapa vai no seu git hub> settings > SSH e GPG keys > New SSH> coloque o titulo + a sua chave sem mudar a key type e pronto!

Agora é só você fazer o git remote usando o ssh e quando aparecer uma pergunta após o git push é apenas escrever o sim(yes) e a partir desse momento todos os seus git remotes já vão estar configurados com o seu SSH!
