---
title: Utilizando o RDS com o pool de conexão ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7baaf81d7a5d6a91416ea5baf8ba57745612740e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462314"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="2eae0-102">Utilizando o RDS com o pool de conexão ODBC</span><span class="sxs-lookup"><span data-stu-id="2eae0-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="2eae0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2eae0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2eae0-p101">Se você estiver usando uma fonte de dados ODBC, poderá utilizar a opção de pool de conexão no IIS (Internet Information Services, Serviços de Informação de Internet) para alcançar alto desempenho ao manipular a carga do cliente. O pool de conexão é um gerenciador de recursos para conexões, mantendo o estado aberto em conexões utilizadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="2eae0-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="2eae0-106">Para ativar o pooling de conexão, consulte a documentação do IIS.</span><span class="sxs-lookup"><span data-stu-id="2eae0-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="2eae0-107">Observe que ativar o pooling de conexão pode sujeitar o servidor Web a outras restrições, como explicado na documentação do Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="2eae0-107">Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="2eae0-108">Para garantir que o pooling de conexão seja estável e forneça ganho adicionais de desempenho, você deve configurar o Microsoft SQL Server para utilizar a biblioteca de rede de Soquete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="2eae0-109">Para fazer isso, você precisa:</span><span class="sxs-lookup"><span data-stu-id="2eae0-109">To do this, you need to:</span></span>

  - <span data-ttu-id="2eae0-110">Configurar o computador SQL Server para usar Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="2eae0-111">Configurar o servidor Web para usar Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-111">Configure the Web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="2eae0-112">Configurando o computador SQL Server para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="2eae0-113">No computador SQL Server, execute o programa de configuração do SQL Server para que as interações com a fonte de dados utilizem a biblioteca de rede de Soquete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="2eae0-114">**Para especificar a biblioteca de rede de Soquete TCP/IP no computador SQL Server**</span><span class="sxs-lookup"><span data-stu-id="2eae0-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="2eae0-115">**No Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="2eae0-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="2eae0-116">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **Instalação SQL**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="2eae0-117">Clique em **Continuar** duas vezes.</span><span class="sxs-lookup"><span data-stu-id="2eae0-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="2eae0-118">Na caixa de diálogo **Microsoft SQL Server  Opções**, selecione **Alterar suporte à rede** e, em seguida, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="2eae0-119">Certifique-se de que a caixa de seleção **Soquetes TCP/IP** esteja marcada e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="2eae0-120">Clique em **Continuar** para finalizar e sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="2eae0-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="2eae0-121">**No Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="2eae0-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="2eae0-122">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="2eae0-123">Na guia **Geral** da caixa de diálogo, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="2eae0-124">Na caixa de diálogo **Adicionar configuração da biblioteca de rede**, clique em **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="2eae0-125">Nas caixas **Número da porta** e **Endereço de proxy**, digite o número da porta e o endereço de proxy fornecidos pelo administrador da rede.</span><span class="sxs-lookup"><span data-stu-id="2eae0-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="2eae0-126">Clique em **OK** para finalizar e sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="2eae0-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="2eae0-127">Configurando o servidor Web para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-127">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="2eae0-p102">Há duas opções para configurar o servidor Web para usar soquetes TCP/IP. O que você faz depende de todos os SQL Servers serem acessados do servidor Web ou apenas de um SQL Server específico ser acessado do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="2eae0-p102">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="2eae0-p103">Se todos os SQL Servers forem acessados do servidor Web, será necessário executar o SQL Server Client Configuration Utility no computador do servidor Web. As seguintes etapas alteram a biblioteca de rede padrão para todas as conexões do SQL Server feitas desse servidor para usar a biblioteca de rede de Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-p103">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="2eae0-132">**Para configurar o servidor Web (todos os SQL Servers)**</span><span class="sxs-lookup"><span data-stu-id="2eae0-132">**To configure the Web server (all SQL Servers)**</span></span>

<span data-ttu-id="2eae0-133">**Para Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="2eae0-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="2eae0-134">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="2eae0-135">Clique na guia **Biblioteca de rede**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="2eae0-136">Na caixa **Rede padrão**, selecione **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="2eae0-137">Clique em **Concluído** para salvar as alterações e sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="2eae0-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="2eae0-138">**Para Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="2eae0-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="2eae0-139">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="2eae0-140">Clique na guia **Geral**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="2eae0-141">Na caixa **Biblioteca de rede padrão**, clique em **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="2eae0-142">Clique em **OK** para salvar as alterações e sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="2eae0-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="2eae0-p104">Se um SQL Server específico for acessado de um servidor Web, você precisará executar o SQL Server Client Configuration Utility no computador do servidor Web. Para alterar a biblioteca de rede para uma conexão específica do SQL Server, configure o software SQL Server Client no computador do servidor Web como se segue.</span><span class="sxs-lookup"><span data-stu-id="2eae0-p104">If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<span data-ttu-id="2eae0-145">**Para configurar o servidor Web (um SQL Server específico)**</span><span class="sxs-lookup"><span data-stu-id="2eae0-145">**To configure the Web server (a specific SQL Server)**</span></span>

<span data-ttu-id="2eae0-146">**Para Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="2eae0-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="2eae0-147">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="2eae0-148">Clique na guia **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="2eae0-149">Na caixa **Servidor**, digite o nome do servidor para conexão utilizando **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="2eae0-150">Na caixa **Nome DLL**, selecione **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="2eae0-p105">Clique em **Adicionar/modificar**. Todas as fontes de dados apontando para esse servidor utilizarão Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2eae0-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="2eae0-153">Clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-153">Click **Done**.</span></span>

<span data-ttu-id="2eae0-154">**Para Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="2eae0-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="2eae0-155">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="2eae0-156">Clique na guia **Geral**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="2eae0-157">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="2eae0-157">Click **Add**.</span></span>

4.  <span data-ttu-id="2eae0-p106">Digite o alias do servidor na caixa **Alias de servidor**. Na caixa **Bibliotecas de rede**, clique em **TCP/IP**. Na caixa **Nome do computador**, digite o nome do computador que atende os clientes de Soquetes TCP/IP. Na caixa **Número da porta**, digite a porta na qual o SQL Server atende.</span><span class="sxs-lookup"><span data-stu-id="2eae0-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="2eae0-162">Clique em **OK** e, em seguida, em **OK** novamente para sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="2eae0-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

