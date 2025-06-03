#Comandos usados em aula

## 💻 Comandos CMD úteis

ipconfig /all        # Mostra detalhes da rede local
ping 8.8.8.8         # Verifica conexão com a internet
tracert google.com   # Rastreia o caminho até um site
netstat -an          # Lista conexões abertas
whoami               # Exibe o usuário logado
systeminfo           # Detalhes sobre o sistema operacional

##🔍 Comandos Básicos de Rede
ipconfig /all  # Mostra todos os detalhes da configuração de rede
ping [alvo] -t # Ping contínuo (usar Ctrl+C para parar)
tracert [alvo] # Rastreia rota até o destino
netstat -ano   # Mostra todas as conexões e ports abertos com PIDs
arp -a         # Exibe a tabela ARP do sistema
route print    # Mostra a tabela de roteamento

##🛡️ Comandos de Segurança
whoami /priv   # Mostra privilégios do usuário atual
net user       # Lista usuários do sistema
net localgroup administrators # Lista administradores do sistema
tasklist /svc # Lista processos em execução com serviços
schtasks /query # Lista tarefas agendadas

##🔧 Comandos de Administração
systeminfo | findstr /B /C:"OS Name" /C:"OS Version" - Mostra versão do OS
wmic qfe get Caption,Description,HotFixID,InstalledOn - Lista updates instalados
driverquery - Lista todos os drivers instalados
gpresult /r - Mostra políticas de grupo aplicadas

##🕵️ Comandos Nmap (requer instalação)
nmap -sP [alvo] # Ping scan (descobre hosts ativos)
nmap -sS [alvo] # SYN scan (varredura stealth)
nmap -sV [alvo] # Detecta versões de serviços
nmap -O [alvo]  # Detecta sistema operacional
nmap -A [alvo]  # Varredura agressiva (OS, versões, scripts)
nmap -p 1-65535 [alvo] # Varredura completa de todas as portas
nmap --script vuln [alvo] # Procura por vulnerabilidades conhecidas

##📊 Comandos Úteis para Análise
findstr /s /i "palavra" *.* # Busca arquivos por conteúdo
certmgr.msc # Gerenciador de certificados
eventvwr.msc # Visualizador de eventos
wevtutil qe Security /rd:true /f:text # Exporta logs de segurança

##🚨 Comandos para Troubleshooting
netsh firewall show state #  Mostra status do firewall
netsh advfirewall show allprofiles # Mostra configurações do firewall avançado
chkdsk /f #  Verifica e repara erros no disco
sfc /scannow #  Verifica e repara arquivos do sistema
