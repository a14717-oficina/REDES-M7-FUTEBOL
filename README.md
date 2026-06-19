# REDES-M7-FUTEBOM7 Futebol Premium - Gestor de Clubes e Jogadores

Descrição

O projeto M7 Futebol Premium é uma aplicação web moderna e responsiva, desenvolvida para a gestão de clubes e jogadores de futebol. A aplicação oferece uma interface de utilizador intuitiva com um design premium, utilizando o conceito de glassmorphism e um tema escuro. O backend é totalmente gerido através do Supabase, uma plataforma de código aberto que fornece funcionalidades de base de dados, autenticação e armazenamento, permitindo uma gestão eficiente e escalável dos dados.

Funcionalidades

•
Navegação Responsiva: Uma barra de navegação adaptável a diferentes tamanhos de ecrã, com links para as secções de Clubes, Jogadores e Adicionar Jogador.

•
Dashboard Interativo: Uma secção principal que serve como gestor, destacando a capacidade de gerir clubes e jogadores.

•
Adicionar Jogador: Um formulário dedicado para a inserção de novos jogadores na base de dados, com validação de campos para garantir a integridade dos dados.

•
Listagem Dinâmica de Clubes: Exibe uma lista de clubes, carregada dinamicamente do Supabase, com detalhes como nome do clube e país. Os cartões dos clubes apresentam um efeito visual de hover.

•
Listagem Dinâmica de Jogadores: Apresenta uma lista detalhada de jogadores, também carregada do Supabase, incluindo nome, posição, clube, país e idade. Cada cartão de jogador permite ações de edição (placeholder) e eliminação.

•
Gestão de Dados em Tempo Real: Integração com o Supabase para operações CRUD (Criar, Ler, Atualizar, Apagar) de jogadores e leitura de clubes.

•
Mensagens de Feedback: Notificações visuais para o utilizador sobre o sucesso ou falha das operações.

Tecnologias Utilizadas

O projeto M7 Futebol Premium foi construído com as seguintes tecnologias:

•
HTML5: Para a estrutura e conteúdo da página web.

•
CSS3: Para o design e estilização da interface, incluindo:

•
Glassmorphism: Efeito visual moderno com elementos translúcidos e desfocados.

•
Tema Escuro: Estética premium com cores escuras e gradientes vibrantes.

•
Fontes: Utilização das fontes Inter e Poppins para uma tipografia clara e apelativa.



•
JavaScript: Para a lógica de frontend, manipulação do DOM e interação com o Supabase.

•
Supabase: Como solução de Backend-as-a-Service (BaaS), fornecendo:

•
Base de Dados PostgreSQL: Para armazenar os dados de clubes e jogadores.

•
API RESTful: Para a comunicação entre o frontend e a base de dados.



Estrutura do Projeto

O projeto está organizado da seguinte forma:

Plain Text


M7-FUTEBOL/
├── index.html
├── script.js
└── style.css



•
index.html: O ficheiro principal que define a estrutura da página web e inclui as secções de navegação, hero, formulário de adição, listagens de clubes e jogadores, e o rodapé.

•
script.js: Contém toda a lógica JavaScript da aplicação, incluindo a inicialização do cliente Supabase, funções para carregar e exibir clubes e jogadores, e a gestão de eventos para adicionar, editar e apagar jogadores.

•
style.css: Define todos os estilos visuais da aplicação, desde as variáveis de cor e tipografia até aos layouts responsivos e efeitos de glassmorphism.

Configuração do Supabase

Para que a aplicação funcione corretamente, é necessário configurar um projeto no Supabase e criar as tabelas clube e jogador.

Credenciais

As credenciais do Supabase são definidas no ficheiro script.js:

JavaScript


const SUPABASE_URL = 'https://kavidbsevngoevanekmo.supabase.co';
const SUPABASE_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImthdmlkYnNldm5nb2V2YW5la21vIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzgxNDY0OTgsImV4cCI6MjA5MzcyMjQ5OH0.9WkpJKjBVOTUS7gj2EteQbZhmgZsRAoW3Aklyaz2G7g';



ATENÇÃO: Por motivos de segurança, estas chaves devem ser tratadas com cuidado. Em ambientes de produção, é recomendável utilizar variáveis de ambiente para armazenar as chaves API e evitar expô-las diretamente no código frontend.

Estrutura das Tabelas

As tabelas necessárias na sua base de dados Supabase são:

Tabela clube:

Coluna
Tipo
Notas
nomeclube
TEXT
Chave Primária, Único
pais
TEXT


estadio
TEXT






Tabela jogador:

Coluna
Tipo
Notas
numatleta
INT
Chave Primária, Auto-Incremento
nomejogador
TEXT


pais
TEXT


idade
INT


posicao
TEXT


nomeclube
TEXT
Chave Estrangeira para clube.nomeclube
imagens
TEXT
URL da imagem do jogador (opcional )




Certifique-se de que as políticas de RLS (Row Level Security) no Supabase estão configuradas para permitir as operações de leitura, inserção e eliminação necessárias para a aplicação.

Instalação e Uso

1.
Clonar o Repositório: Faça o download ou clone este repositório para o seu ambiente local.

2.
Configurar Supabase: Crie um novo projeto no Supabase. Crie as tabelas clube e jogador com as estruturas acima. Preencha a tabela clube com alguns dados iniciais (ex: FC Porto, Real Madrid, Barcelona, AC Milan, Manchester United).

3.
Atualizar Credenciais: No ficheiro script.js, substitua SUPABASE_URL e SUPABASE_KEY pelas credenciais do seu projeto Supabase.

4.
Abrir no Navegador: Abra o ficheiro index.html diretamente no seu navegador web preferido. Não é necessário um servidor web para esta aplicação, pois todas as operações de backend são tratadas pelo Supabase.

