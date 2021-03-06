---
title: Utilizando o RDS com o pool de conexão ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87d380fdc52cdee2aa834fd6e78ff1b761a0e93a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312114"
---
# <a name="using-rds-with-odbc-connection-pooling"></a>Uso do RDS com pool de conexão ODBC


**Aplica-se ao:** Access 2013, Office 2013

Se você estiver usando uma fonte de dados ODBC, poderá utilizar a opção de pool de conexão no IIS (Internet Information Services, Serviços de Informação de Internet) para alcançar alto desempenho ao manipular a carga do cliente. O pool de conexão é um gerenciador de recursos para conexões, mantendo o estado aberto em conexões utilizadas com frequência.

Para ativar o pooling de conexão, consulte a documentação do IIS.

Observe que a habilitação do pooling de conexões pode sujeitar o servidor Web a outras restrições, conforme anotado na documentação dos Serviços de Informações da Internet da Microsoft.

Para garantir que o pooling de conexão seja estável e forneça ganho adicionais de desempenho, você deve configurar o Microsoft SQL Server para utilizar a biblioteca de rede de Soquete TCP/IP.

Para fazer isso, você precisa:

  - Configurar o computador SQL Server para usar Soquetes TCP/IP.

  - Configure o servidor Web para usar soquetes TCP/IP.

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

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a>Configurando o servidor Web para usar soquetes TCP/IP

Há duas opções para configurar o servidor Web para usar Soquetes TCP/IP. O que você faz depende se todos os SQL Servers são acessados a partir do servidor Web ou apenas um SQL Server específico é acessado a partir do servidor Web.

Se todos os SQL Servers são acessados a partir do servidor Web, você precisa executar o SQL Server Client Configuration Utility no computador do servidor Web. As etapas a seguir alteram a biblioteca de rede padrão para todas as conexões do SQL Server feitas a partir desse servidor Web do IIS para usar a biblioteca de rede de Soquetes TCP/IP.

**Para configurar o servidor Web (todos os SQL Servers)**

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

Se um SQL Server específico for acessado a partir de um servidor Web, você precisará executar o Utilitário de Configuração de Cliente do SQL Server no computador do servidor Web. Para alterar a biblioteca de rede de uma conexão específica do SQL Server, configure o software sql Server Client no computador servidor Web da seguinte forma.

**Para configurar o servidor Web (um SQL Server específico)**

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

