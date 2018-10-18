---
title: Utilizando o RDS com o pool de conexão ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee66e68cb8eeaaca57c007dc64a9e2b3a8476ec7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606014"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>Utilizando o RDS com o pool de conexão ODBC


**Aplica-se a**: Access 2013 | Office 2013

Se você estiver usando uma fonte de dados ODBC, poderá utilizar a opção de pool de conexão no IIS (Internet Information Services, Serviços de Informação de Internet) para alcançar alto desempenho ao manipular a carga do cliente. O pool de conexão é um gerenciador de recursos para conexões, mantendo o estado aberto em conexões utilizadas com frequência.

Para ativar o pooling de conexão, consulte a documentação do IIS.

<<<<<<< Cabeça por favor, observe que ativar o pooling de conexão pode sujeitar o servidor Web a outras restrições, conforme indicado na documentação do Microsoft Internet Information Services.
=== Observe que ativar o pooling de conexão pode sujeitar o servidor web a outras restrições, conforme indicado na documentação do Microsoft Internet Information Services.
>>>>>>> mestre

Para garantir que o pooling de conexão seja estável e forneça ganho adicionais de desempenho, você deve configurar o Microsoft SQL Server para utilizar a biblioteca de rede de Soquete TCP/IP.

Para fazer isso, você precisa:

  - Configurar o computador SQL Server para usar Soquetes TCP/IP.

<<<<<<< Cabeça
  - Configurar o servidor Web para usar Soquetes TCP/IP.
=======
  - Configure o servidor web para usar soquetes TCP/IP.
>>>>>>> mestre

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a>Configurando o computador SQL Server para usar soquetes TCP/IP.

No computador SQL Server, execute o programa de configuração do SQL Server para que as interações com a fonte de dados utilizem a biblioteca de rede de Soquete TCP/IP.

**Para especificar a biblioteca de rede de Soquete TCP/IP no computador SQL Server**

**No Microsoft SQL Server 6.5:**

1.  No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **Instalação SQL**.

2.  Clique em **Continuar** duas vezes.

3.  Na caixa de diálogo **Microsoft SQL Server  Opções**, selecione **Alterar suporte à rede** e, em seguida, clique em **Continuar**.

4.  Certifique-se de que a caixa de seleção **Soquetes TCP/IP** esteja marcada e clique em **OK**.

5.  Clique em **Continuar** para finalizar e sair da instalação.

**No Microsoft SQL Server 7.0:**

1.  No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Server Network Utility**.

2.  Na guia **Geral** da caixa de diálogo, clique em **Adicionar**.

3.  Na caixa de diálogo **Adicionar configuração da biblioteca de rede**, clique em **TCP/IP**.

4.  Nas caixas **Número da porta** e **Endereço de proxy**, digite o número da porta e o endereço de proxy fornecidos pelo administrador da rede.

5.  Clique em **OK** para finalizar e sair da instalação.

<<<<<<< Cabeça
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Configurando o servidor Web para usar soquetes TCP/IP.

Há duas opções para configurar o servidor Web para usar soquetes TCP/IP. O que você faz depende de todos os SQL Servers serem acessados do servidor Web ou apenas de um SQL Server específico ser acessado do servidor Web.

Se todos os SQL Servers forem acessados do servidor Web, será necessário executar o SQL Server Client Configuration Utility no computador do servidor Web. As seguintes etapas alteram a biblioteca de rede padrão para todas as conexões do SQL Server feitas desse servidor para usar a biblioteca de rede de Soquetes TCP/IP.

<a name="to-configure-the-web-server-all-sql-servers"></a>**Para configurar o servidor Web (todos os SQL Servers)**
=======
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Configurando o servidor para usar soquetes de TCP/IP na web

Há duas opções para configurar o servidor web para usar soquetes TCP/IP. O que fazer depende se todos os SQL Servers são acessados a partir do servidor web ou apenas um SQL Server específico é acessado a partir do servidor web.

Se todos os SQL Servers são acessados a partir do servidor web, você precisará executar o utilitário de configuração do cliente SQL Server no computador do servidor web. As etapas a seguir alteram a biblioteca de rede padrão para todas as conexões do SQL Server feitas a partir deste servidor de web IIS para usar a biblioteca de rede soquetes TCP/IP.

**Para configurar o servidor web (todos os SQL Servers)**
>>>>>>> mestre

**Para Microsoft SQL Server 6.5:**

1.  No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.

2.  Clique na guia **Biblioteca de rede**.

3.  Na caixa **Rede padrão**, selecione **Soquetes TCP/IP**.

4.  Clique em **Concluído** para salvar as alterações e sair do utilitário.

**Para Microsoft SQL Server 7.0:**

1.  No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Network Utility**.

2.  Clique na guia **Geral**.

3.  Na caixa **Biblioteca de rede padrão**, clique em **TCP/IP**.

4.  Clique em **OK** para salvar as alterações e sair do utilitário.

<<<<<<< Cabeça se um SQL Server específico é acessado a partir de um servidor Web, você precisará executar o utilitário de configuração do cliente SQL Server no computador do servidor Web. Para alterar a biblioteca de rede para uma conexão específica do SQL Server, configure o software SQL Server Client no computador do servidor Web como se segue.

<a name="to-configure-the-web-server-a-specific-sql-server"></a>**Para configurar o servidor Web (um SQL Server específico)**
=======
Se um SQL Server específico é acessado a partir de um servidor web, você precisará executar o utilitário de configuração do cliente SQL Server no computador do servidor web. Para alterar a biblioteca de rede para uma conexão do SQL Server específico, configure o software de cliente do SQL Server no computador do servidor web da seguinte maneira.

**Para configurar o servidor web (um SQL Server específico)**
>>>>>>> mestre

**Para Microsoft SQL Server 6.5:**

1.  No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.

2.  Clique na guia **Avançado**.

3.  Na caixa **Servidor**, digite o nome do servidor para conexão utilizando **Soquetes TCP/IP**.

4.  Na caixa **Nome DLL**, selecione **Soquetes TCP/IP**.

5.  Clique em **Adicionar/modificar**. Todas as fontes de dados apontando para esse servidor utilizarão Soquetes TCP/IP.

6.  Clique em **Concluído**.

**Para Microsoft SQL Server 7.0:**

1.  No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Configuration Utility**.

2.  Clique na guia **Geral**.

3.  Clique em **Adicionar**.

4.  Digite o alias do servidor na caixa **Alias de servidor**. Na caixa **Bibliotecas de rede**, clique em **TCP/IP**. Na caixa **Nome do computador**, digite o nome do computador que atende os clientes de Soquetes TCP/IP. Na caixa **Número da porta**, digite a porta na qual o SQL Server atende.

5.  Clique em **OK** e, em seguida, em **OK** novamente para sair do utilitário.

