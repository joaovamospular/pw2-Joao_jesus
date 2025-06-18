# 🛠️ Guia de Instalação e Uso do Laravel com Composer, Node.js e Vue

## 📌 Introdução

Este guia apresenta os passos para instalação do Laravel, configuração de ambiente e criação de um projeto Laravel com Vue.js, utilizando **Composer**, **Node.js**, **Laravel Installer** e **XAMPP**.

---

## ⚙️ Pré-requisitos

Antes de começar, certifique-se de que você possui os seguintes itens instalados:

- **PHP 8.1+**: Linguagem base do Laravel.
- **Composer**: Gerenciador de dependências PHP.
- **Node.js e npm**: Necessários para compilar assets e frontend.
- **XAMPP/WAMP**: Para simular ambiente local com servidor Apache e MySQL.
- **Laravel Installer**: Ferramenta para criar projetos Laravel via terminal.

---

## ✅ Verificações de Instalação

### Verificar o Composer

```bash
composer -v
```

### Verificar o Node.js

```bash
node -v
```

---

## 🧱 Instalação do Laravel Installer

Execute:

```bash
composer global require laravel/installer
```

> Certifique-se de que o diretório do Composer está no PATH do sistema.

---

## 🧪 Testar a Instalação

Após instalar, crie seu projeto com:

```bash
laravel new nome-do-projeto
```

O terminal solicitará:

- **Kit de inicialização** (recomenda-se `vue`).
- **Autenticação** (use a opção padrão do Laravel).

---

## 📁 Acesse a pasta do projeto

```bash
cd nome-do-projeto
```

---

## ⚙️ Configuração do Ambiente

Copie o arquivo `.env.example`:

```bash
cp .env.example .env
php artisan key:generate
```

---

## 🗄️ Configure seu banco de dados

Edite o arquivo `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nome_banco
DB_USERNAME=root
DB_PASSWORD=senha
```

---

## 🔄 Execute as Migrations (opcional)

```bash
php artisan migrate
```

---

## 🧪 Testar no navegador

```bash
php artisan serve
```

Acesse: [http://localhost:8000](http://localhost:8000)

---

## 🎨 Instalar dependências frontend e compilar assets

```bash
npm install && npm run build
```

> Instala bibliotecas JS e compila arquivos para produção.

---

## 🚀 Ambiente completo de desenvolvimento

```bash
composer run dev
```

Este comando ativa:

- `php artisan serve`: servidor local.
- Queue worker: tarefas em segundo plano.
- Vite: atualiza frontend automaticamente.

---

## 📎 Dica

Caso o Composer não reconheça o PHP, indique manualmente o executável no instalador (ex: `xampp/php/php.exe`).

---

Pronto! Seu ambiente Laravel com Vue está configurado e pronto para o desenvolvimento!


# 🚀 Criando uma Aplicação Laravel

## 📦 Instalando o PHP e o Laravel Installer

Antes de criar sua primeira aplicação Laravel, certifique-se de que sua máquina possui os seguintes itens instalados:

- **PHP**
- **Composer**
- **Laravel Installer**
- **Node + NPM** (ou Bun) – para compilar os assets do frontend

### ✅ Instalação via Script

Se você **ainda não tem o PHP e o Composer instalados**, execute o seguinte comando no **PowerShell do Windows como administrador**:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; `
[System.Net.ServicePointManager]::SecurityProtocol = `
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; `
iex ((New-Object System.Net.WebClient).DownloadString('https://php.new/install/windows/8.4'))
```

> Após executar o comando, **reinicie o terminal**.  
> Para atualizar o PHP, Composer e Laravel Installer, execute novamente o mesmo comando no futuro.

### 💡 Se você já tem o PHP e o Composer instalados

Instale o Laravel Installer com:

```bash
composer global require laravel/installer
```

> Para uma experiência gráfica e completa de instalação e gerenciamento do PHP, você pode utilizar o [Laravel Herd](https://herd.laravel.com).

---

## 🛠 Criando a Aplicação Laravel

Com tudo instalado, crie sua aplicação Laravel com o comando:

```bash
laravel new exemplo-app
```

Durante o processo, você poderá escolher:

- Framework de testes
- Banco de dados
- Kit inicial (Vue, React, Livewire, etc.)

---

## 🚧 Executando a Aplicação

Acesse a pasta do projeto:

```bash
cd exemplo-app
```

Instale as dependências do frontend e compile os arquivos:

```bash
npm install && npm run build
```

Inicie o ambiente completo de desenvolvimento:

```bash
composer run dev
```

Esse comando irá:

- Rodar o **servidor local Laravel** em [http://localhost:8000](http://localhost:8000)
- Ativar o **queue worker** (tarefas em segundo plano)
- Iniciar o **Vite** para recarregamento automático do frontend

---

Pronto! Agora você pode começar a desenvolver sua aplicação com Laravel!
