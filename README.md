# Guia de Instalação do Laravel e Execução de Migrations

Este guia mostra, com comandos e prints, como:
1. Instalar o instalador do Laravel
2. Criar um novo projeto
3. Configurar o banco
4. Instalar/buildar assets com npm
5. Executar as migrations
6. Criar uma migration customizada
7. Rodar as migrations novamente

> **Requisitos**
> - PHP 8.2+ com extensões comuns (pdo, mbstring, openssl, tokenizer, xml, ctype, json)  
> - Composer  
> - Node.js + npm  
> - MySQL/MariaDB (ou outro driver compatível)  
> - (Opcional) XAMPP/WAMP para ambiente local no Windows

## 1) Instalar o instalador do Laravel (Composer)

**Comando:**
```bash
composer global require laravel/installer
```

**Print:**

<img width="1150" height="325" alt="pt 1" src="https://github.com/user-attachments/assets/ecea0411-ee2e-486b-aad9-ec42effc6af2" />

 
## 2) Criar um novo projeto Laravel

**Comando:**
```bash
laravel new 'nome-da-aplicação'
```

**Print:**

<img width="547" height="160" alt="pt 2-1" src="https://github.com/user-attachments/assets/8f22be35-743a-47b3-a9df-70d932b46a9c" />



## 3) Configurar a aplicação Laravel

**Prints:**

<img width="547" height="212" alt="pt 2-2" src="https://github.com/user-attachments/assets/4e9fc516-1774-40a3-bc51-fcf276471f71" />


<img width="635" height="142" alt="pt 3" src="https://github.com/user-attachments/assets/5505ab62-43d1-4231-9bd8-903031aa0e4b" />




Observação: Escolher **não** criar o banco de dados com as migrations padrão
```bash
Default database updated. Would you like to run the default database migrations? (yes/no) [yes]:
 > no
```


## 4) Instalar dependências e gerar build

**Comando:**
```bash
npm install
npm run build
```

*ou*

**Print:**

<img width="726" height="511" alt="pt 4" src="https://github.com/user-attachments/assets/e790e87b-d99a-4d65-bdf2-8a01a584ac2c" />



## 5) Configurar o .env de acordo com o .env.example, e executar as migrations para assim criar o banco de dados

**Arquivo .env:**
```bash
APP_NAME="Laravel"
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=bd_escola
DB_USERNAME=root
DB_PASSWORD=
```

**Confirmar que a chave da aplicação foi gerada corretamente:**

<img width="419" height="73" alt="5-1" src="https://github.com/user-attachments/assets/86d16c83-772e-4055-9e57-af7346612dcc" />


**Print das Migrations:**

<img width="619" height="236" alt="pt 5" src="https://github.com/user-attachments/assets/fc6b9f9e-0bba-4329-9dff-c0a2d966539c" />


## 6) Criar uma migration customizada (ex.: create_aluno)

**Comando:**
```bash
php artisan make:migration create_aluno
```

**Print:**

<img width="1004" height="85" alt="pt 6" src="https://github.com/user-attachments/assets/373a7432-0c7b-443a-b143-92bd24955781" />


Após a criação da migration, edite o arquivo da migration para então criar os campos da tabela criada



## 7) Rodar as migrations novamente

**Comando:**
```bash
php artisan migrate
```

**Print:**

<img width="594" height="103" alt="pt 7" src="https://github.com/user-attachments/assets/08d1bd42-33b5-48c2-b661-f01f98fe9332" />


