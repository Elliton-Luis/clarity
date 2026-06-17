# Clarity | 24h Challenge
Um desafio pessoal de desenvolvimento em tempo fechado (24h): o quão longe é possível ir criando uma aplicação do zero, priorizando uma interface limpa, velocidade de entrega e o conceito de "aprender fazendo".

## O Projeto
O projeto consiste num gestor de tarefas completo, seguro e multiutilizador, focado em colocar em prática os recursos do ecossistema Laravel.

### O Desafio & Aprendizados
A proposta não era apenas criar mais um CRUD comum, mas sim testar a velocidade de resposta e absorção de novos conceitos sob pressão de tempo:
* **Roteamento & Facades**: Uso aprofundado dos recursos nativos do Laravel para acelerar a criação de endpoints e estruturação limpa dos controllers.
* **Persistência Segura**: Implementação prática de Soft Deletes (Lixeira) para controlo e recuperação de dados por parte do utilizador.
* **Interface sob Pressão**: Construção de uma UI responsiva e fluida utilizando Tailwind CSS e Alpine.js dentro do prazo estabelecido.

## Funcionalidades
* **Autenticação Isolada**: Sistema completo de login e registo. Cada utilizador gere estritamente os seus próprios dados.
* **Gestão de Tarefas (CRUD)**: Criação, edição, visualização e listagem dinâmica com filtros por status (pendente/concluída).
* **Sistema de Lixeira (Soft Deletes)**: Itens excluídos são movidos para uma lixeira interna, permitindo restauração ou exclusão definitiva.

## Interface (UI) e Responsividade

O projeto **Clarity** foi desenhado com foco total na experiência do usuário, apresentando uma interface limpa, intuitiva e moderna com Tailwind CSS. O design é **totalmente responsivo**, adaptando-se perfeitamente a desktops, tablets e smartphones.

### Visualização Desktop

<p align="center">
  <img src="https://github.com/user-attachments/assets/17f817ad-d384-4e84-aa32-767664547936" width="49%" alt="Dashboard Principal" title="Dashboard Principal">
  <img src="https://github.com/user-attachments/assets/a4323f85-114e-45cf-b274-10128267980b" width="49%" alt="Lixeira e Soft Deletes" title="Lixeira">
</p>
<p align="center">
  <em>Esquerda: Lista principal de tarefas com layout dinâmico. Direita: Sistema de lixeira isolado para recuperação de tarefas (Soft Deletes).</em>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/7f2d5433-fb6f-4cdb-ae11-3975df6188b8" width="49%" alt="Formulário de Criação" title="Criar Nova Tarefa">
  <img src="https://github.com/user-attachments/assets/6263756b-5cfd-4ac7-a42f-02b62aa2b364" width="49%" alt="Tela de Detalhes" title="Detalhes da Tarefa">
</p>
<p align="center">
  <em>Esquerda: Formulário simplificado para inserção rápida de dados. Direita: Visualização detalhada das informações da tarefa.</em>
</p>

### Visualização Mobile (Mobile-First)

A navegação foi pensada para manter a fluidez em qualquer tamanho de tela, empilhando elementos de forma lógica e mantendo os botões de ação acessíveis.

<p align="center">
  <img src="https://github.com/user-attachments/assets/47f75299-01da-4216-a60c-a8c3847cc235" width="24%" alt="Lista Mobile" title="Lista Mobile">
  <img src="https://github.com/user-attachments/assets/489f7b6b-00e0-43ee-9312-c5265a74c621" width="24%" alt="Lixeira Mobile" title="Lixeira Mobile">
  <img src="https://github.com/user-attachments/assets/d9a69098-7554-44f4-86aa-85b254a86b71" width="24%" alt="Formulário Mobile" title="Formulário Mobile">
  <img src="https://github.com/user-attachments/assets/84afed6c-d3ca-4cc5-9a17-e9093793d213" width="24%" alt="Detalhes Mobile" title="Detalhes Mobile">
</p>
<p align="center">
  <em>Fluxo completo responsivo: Visão Geral, Lixeira, Criação de Tarefa e Detalhes perfeitamente adaptados para telas menores.</em>
</p>

## Tecnologias
* **Back-end**: Laravel 11 / PHP 8.2+
* **Front-end**: Blade Views, Tailwind CSS, Alpine.js
* **Base de Dados**: SQLite (padrão de desenvolvimento) / Suporta qualquer base relacional mudando o .env

## Instalação e Execução Local
A aplicação vem configurada por padrão com SQLite, eliminando a necessidade de iniciar contentores ou servidores locais de bases de dados para testar.

### Pré-requisitos
* PHP >= 8.2
* Composer
* Node.js & NPM

### Passo a Passo
1. Clone o repositório e acesse o diretório:
```bash
git clone https://github.com/Elliton-Luis/to-do-list
cd to-do-list
```
2. Instale as dependências do ecossistema PHP:
```bash
composer install
```
3. Configure o ambiente e gere a chave única da aplicação:
```
cp .env.example .env
php artisan key:generate
```
4. Crie o ficheiro do SQLite e execute as migrations:
```bash
php artisan migrate
```
5. Instale e compile os assets do front-end:
```bash
npm install
npm run dev
```
6. Com a compilação do front-end a correr, abra um segundo terminal e inicie o servidor interno do Laravel:
```bash
php artisan serve
```
7. Aceda através do navegador em: [http://127.0.0.1:8000](http://127.0.0.1:8000)
