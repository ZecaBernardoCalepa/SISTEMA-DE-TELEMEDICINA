🏥 SISTEMA DE TELEMEDICINA
Sistema de Telemedicina desenvolvido em Laravel, no âmbito da disciplina de Sistemas Distribuídos.
A plataforma permite aproximar pacientes e profissionais de saúde, disponibilizando funcionalidades para gestão de utilizadores, consultas.

📋 Sobre o Projecto
O Sistema de Telemedicina foi desenvolvido com o objectivo de demonstrar a aplicação prática de conceitos de Sistemas Distribuídos na área da saúde.
________________________________________
🚀 Funcionalidades
👤 Gestão de Utilizadores
•	Registo de utilizadores
•	Login e logout
•	Recuperação de palavra-passe
•	Gestão de perfil
•	Alteração de palavra-passe
•	Gestão de permissões
•	Diferentes tipos de utilizadores
Tipos de utilizadores
•	Administrador
•	Médico/Profissional de Saúde
•	Paciente
________________________________________
🧑‍⚕️ Gestão de Profissionais de Saúde
O profissional de saúde pode:
•	Criar e actualizar o perfil profissional
•	Informar especialidade
•	Definir disponibilidade
•	Consultar pacientes
•	Consultar consultas agendadas
•	Aceitar ou rejeitar consultas
•	Realizar consultas online
•	Registar informações do atendimento
•	Consultar o histórico dos pacientes autorizados
________________________________________
👨⚕️ Gestão de Pacientes
O paciente pode:
•	Criar uma conta
•	Actualizar os seus dados
•	Consultar profissionais de saúde
•	Pesquisar por especialidade
•	Solicitar consultas
•	Agendar consultas
•	Cancelar consultas
•	Consultar o histórico
•	Participar em consultas online
•	Receber notificações

📅 Gestão de Consultas
O sistema permite:
•	Agendamento de consultas
•	Escolha do profissional
•	Definição da data e hora
•	Descrição do motivo da consulta
•	Confirmação da consulta
•	Cancelamento
•	Alteração do estado da consulta
•	Histórico de consultas
Estados da consulta
Pendente
Confirmada
Em andamento
Concluída
Cancelada



👨‍💼 Painel Administrativo
O administrador pode:
•	Gerir utilizadores
•	Gerir pacientes
•	Gerir profissionais
•	Gerir especialidades
•	Gerir consultas
•	Consultar estatísticas
•	Gerir permissões
•	Consultar actividades do sistema


🛠️ Tecnologias Utilizadas
Backend
•	PHP
•	Laravel
Base de Dados
•	MySQL
Frontend
•	HTML5
•	CSS3
•	JavaScript
•	Blade
Servidor
•	Ubuntu
•	Nginx
•	PHP-FPM
________________________________________
💻 Requisitos
Antes de instalar o projecto, certifique-se de que possui:
•	PHP 8.2 ou superior
•	Composer
•	MySQL
•	Node.js
•	NPM
•	Git
•	Extensões PHP necessárias pelo Laravel
Verificar PHP:
php -v
Verificar Composer:
composer -V
Verificar Node.js:
node -v
Verificar NPM:
npm -v
________________________________________
📥 Instalação
1. Clonar o projecto
git clone https://github.com/SEU-USUARIO/SISTEMA-DE-TELEMEDICINA.git
Entrar na pasta:
cd SISTEMA-DE-TELEMEDICINA
________________________________________
2. Instalar dependências do Laravel
composer install
________________________________________
3. Instalar dependências do Frontend
npm install
________________________________________
4. Criar o ficheiro .env
Copiar o ficheiro de configuração:
cp .env.example .env
No Windows:
copy .env.example .env
________________________________________
5. Gerar a chave da aplicação
php artisan key:generate
________________________________________
6. Criar a Base de Dados
Criar uma base de dados MySQL:
CREATE DATABASE telemedicina;
Depois configurar o ficheiro .env:
APP_NAME="Sistema de Telemedicina"
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://127.0.0.1:8000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=telemedicina
DB_USERNAME=root
DB_PASSWORD=
Altere DB_USERNAME e DB_PASSWORD de acordo com a configuração do seu MySQL.
________________________________________
7. Executar as migrations
php artisan migrate
Caso o projecto possua dados iniciais:
php artisan db:seed
Ou:
php artisan migrate --seed
________________________________________
8. Criar o link do Storage
php artisan storage:link
Este comando permite disponibilizar ficheiros armazenados em storage/app/public.
________________________________________
9. Compilar os ficheiros Frontend
Durante o desenvolvimento:
npm run dev
Para produção:
npm run build
________________________________________
10. Iniciar o servidor Laravel
php artisan serve
O sistema ficará disponível em:
http://127.0.0.1:8000
________________________________________
🔄 Executar Laravel + Vite
Durante o desenvolvimento, podem ser necessários dois terminais.
Terminal 1
php artisan serve
Terminal 2
npm run dev
________________________________________
📡 Configuração do Laravel Reverb
Para funcionalidades em tempo real, como notificações, chat e sinalização da videochamada, pode ser utilizado o Laravel Reverb.
Instalação:
php artisan install:broadcasting
Quando solicitado, seleccione a opção correspondente ao Reverb.
Depois configure o .env de acordo com as credenciais geradas.
Exemplo:
BROADCAST_CONNECTION=reverb

REVERB_APP_ID=telemedicina
REVERB_APP_KEY=telemedicina-key
REVERB_APP_SECRET=telemedicina-secret

REVERB_HOST=127.0.0.1
REVERB_PORT=8080
REVERB_SCHEME=http
Executar o servidor Reverb:
php artisan reverb:start
________________________________________
________________________________________
Em produção, recomenda-se:
APP_ENV=production
APP_DEBUG=false


________________________________________
🧪 Testes
Executar os testes:
php artisan test
Ou:
./vendor/bin/phpunit
________________________________________
🚀 Deploy em Servidor Ubuntu
Para colocar o sistema online:
sudo apt update
sudo apt upgrade
Instalar PHP, MySQL, Nginx, Git, Composer e Node.js.
Depois:
git clone https://github.com/SEU-USUARIO/SISTEMA-DE-TELEMEDICINA.git
cd SISTEMA-DE-TELEMEDICINA

composer install --no-dev --optimize-autoloader

npm install
npm run build

cp .env.example .env

php artisan key:generate
php artisan migrate --force

php artisan storage:link

php artisan config:cache
php artisan route:cache
php artisan view:cache
Configurar o Nginx para apontar para:
/public
e configurar HTTPS através de um certificado SSL.
________________________________________
📌 Estado do Projecto
Backend:          Laravel
Base de Dados:    MySQL
Frontend:         Blade / JavaScript
Videochamada:     WebRTC
Tempo Real:       Laravel Reverb
Servidor:         Ubuntu / Nginx
Estado:           Em desenvolvimento
________________________________________
🔮 Melhorias Futuras
•	Aplicação Android
•	Aplicação iOS
•	Consultas em grupo
•	Partilha de ecrã
•	Chat avançado
•	Notificações Push
•	Integração com hospitais
•	Integração com dispositivos médicos
•	Inteligência Artificial para apoio à triagem
•	Relatórios estatísticos
•	Integração com sistemas laboratoriais
•	Integração com farmácias
•	Prescrição electrónica, conforme os requisitos regulamentares aplicáveis
________________________________________
👨‍💻 Autor
Zeca Bernardo José,Alexandre Yacomba
Projecto desenvolvido no âmbito da disciplina de:
Sistemas Distribuídos
________________________________________
📄 Licença
Este projecto foi desenvolvido para fins académicos e de demonstração.
A utilização em ambiente clínico real deverá considerar os requisitos técnicos, legais, éticos e de segurança aplicáveis à prestação de serviços de saúde.
________________________________________


