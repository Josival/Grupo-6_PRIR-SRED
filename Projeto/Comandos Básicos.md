## Comandos Básicos para utilizarmos no Terminal do Computador

- ``su usuario``: Este comando permite a mudança de usuário em um ambiente shell.

- ``getent passwd``: Este comando lista os usuários do ambiente.

- ``getent group``: Este comando lista os grupos do ambiente.
   
- ``whoami``: Exibe informações de usuário, grupo e privilégios para o usuário que está conectado no sistema local no momento. Se usado sem parâmetros, whoami exibirá o domínio atual e o nome de usuário.
  
- ``hostname``: É utilizado para identificar um sistema em uma rede em qualquer distribuição Linux.
  
- ``pwd``: Informa o diretório absoluto corrente. Por absoluto entende-se que ele mostra o caminho completo desde a raiz do sistema.
  
- ``ls -la``: É usado para visualizar conteúdos em um diretório.
  
- ``cd ~``: Estabelece a raiz inicial do computador como diretório corrente.

- ``cd ..``: Retorna para diretório anterior

* Modificando as permissões de arquivos e pastas:

   * ``chown`` modifica o proprietário da pasta labredes para o usuario nobody e grupo nogroup.
   * ``chgrp`` altera o proprietário de grupo do diretório ``/labredes`` para o grupo ``redes``.
   * ``chmod`` altera as permissões do diretório para escrita pelos membros do grupo.
