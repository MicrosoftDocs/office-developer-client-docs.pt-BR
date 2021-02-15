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
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="e8411-102">Uso do RDS com pool de conexão ODBC</span><span class="sxs-lookup"><span data-stu-id="e8411-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="e8411-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8411-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8411-p101">Se você estiver usando uma fonte de dados ODBC, poderá utilizar a opção de pool de conexão no IIS (Internet Information Services, Serviços de Informação de Internet) para alcançar alto desempenho ao manipular a carga do cliente. O pool de conexão é um gerenciador de recursos para conexões, mantendo o estado aberto em conexões utilizadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="e8411-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="e8411-106">Para ativar o pooling de conexão, consulte a documentação do IIS.</span><span class="sxs-lookup"><span data-stu-id="e8411-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="e8411-107">Observe que a habilitação do pooling de conexões pode sujeitar o servidor Web a outras restrições, conforme anotado na documentação dos Serviços de Informações da Internet da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8411-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="e8411-108">Para garantir que o pooling de conexão seja estável e forneça ganho adicionais de desempenho, você deve configurar o Microsoft SQL Server para utilizar a biblioteca de rede de Soquete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="e8411-109">Para fazer isso, você precisa:</span><span class="sxs-lookup"><span data-stu-id="e8411-109">To do this, you need to:</span></span>

  - <span data-ttu-id="e8411-110">Configurar o computador SQL Server para usar Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="e8411-111">Configure o servidor Web para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="e8411-112">Configurando o computador SQL Server para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="e8411-113">No computador SQL Server, execute o programa de configuração do SQL Server para que as interações com a fonte de dados utilizem a biblioteca de rede de Soquete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="e8411-114">**Para especificar a biblioteca de rede de Soquete TCP/IP no computador SQL Server**</span><span class="sxs-lookup"><span data-stu-id="e8411-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="e8411-115">**No Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="e8411-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="e8411-116">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **Instalação SQL**.</span><span class="sxs-lookup"><span data-stu-id="e8411-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="e8411-117">Clique em **Continuar** duas vezes.</span><span class="sxs-lookup"><span data-stu-id="e8411-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="e8411-118">Na caixa de diálogo **Microsoft SQL Server  Opções**, selecione **Alterar suporte à rede** e, em seguida, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="e8411-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="e8411-119">Certifique-se de que a caixa de seleção **Soquetes TCP/IP** esteja marcada e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8411-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="e8411-120">Clique em **Continuar** para finalizar e sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="e8411-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="e8411-121">**No Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="e8411-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="e8411-122">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="e8411-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="e8411-123">Na guia **Geral** da caixa de diálogo, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e8411-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="e8411-124">Na caixa de diálogo **Adicionar configuração da biblioteca de rede**, clique em **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="e8411-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="e8411-125">Nas caixas **Número da porta** e **Endereço de proxy**, digite o número da porta e o endereço de proxy fornecidos pelo administrador da rede.</span><span class="sxs-lookup"><span data-stu-id="e8411-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="e8411-126">Clique em **OK** para finalizar e sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="e8411-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="e8411-127">Configurando o servidor Web para usar soquetes TCP/IP</span><span class="sxs-lookup"><span data-stu-id="e8411-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="e8411-128">Há duas opções para configurar o servidor Web para usar Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="e8411-129">O que você faz depende se todos os SQL Servers são acessados a partir do servidor Web ou apenas um SQL Server específico é acessado a partir do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="e8411-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="e8411-130">Se todos os SQL Servers são acessados a partir do servidor Web, você precisa executar o SQL Server Client Configuration Utility no computador do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="e8411-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="e8411-131">As etapas a seguir alteram a biblioteca de rede padrão para todas as conexões do SQL Server feitas a partir desse servidor Web do IIS para usar a biblioteca de rede de Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="e8411-132">**Para configurar o servidor Web (todos os SQL Servers)**</span><span class="sxs-lookup"><span data-stu-id="e8411-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="e8411-133">**Para Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="e8411-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="e8411-134">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="e8411-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="e8411-135">Clique na guia **Biblioteca de rede**.</span><span class="sxs-lookup"><span data-stu-id="e8411-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="e8411-136">Na caixa **Rede padrão**, selecione **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="e8411-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="e8411-137">Clique em **Concluído** para salvar as alterações e sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="e8411-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="e8411-138">**Para Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="e8411-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="e8411-139">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="e8411-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="e8411-140">Clique na guia **Geral**.</span><span class="sxs-lookup"><span data-stu-id="e8411-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="e8411-141">Na caixa **Biblioteca de rede padrão**, clique em **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="e8411-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="e8411-142">Clique em **OK** para salvar as alterações e sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="e8411-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="e8411-143">Se um SQL Server específico for acessado a partir de um servidor Web, você precisará executar o Utilitário de Configuração de Cliente do SQL Server no computador do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="e8411-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="e8411-144">Para alterar a biblioteca de rede de uma conexão específica do SQL Server, configure o software sql Server Client no computador servidor Web da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="e8411-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="e8411-145">**Para configurar o servidor Web (um SQL Server específico)**</span><span class="sxs-lookup"><span data-stu-id="e8411-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="e8411-146">**Para Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="e8411-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="e8411-147">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="e8411-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="e8411-148">Clique na guia **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="e8411-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="e8411-149">Na caixa **Servidor**, digite o nome do servidor para conexão utilizando **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="e8411-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="e8411-150">Na caixa **Nome DLL**, selecione **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="e8411-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="e8411-p105">Clique em **Adicionar/modificar**. Todas as fontes de dados apontando para esse servidor utilizarão Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e8411-p105">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="e8411-153">Clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="e8411-153">Click **Done**.</span></span>

<span data-ttu-id="e8411-154">**Para Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="e8411-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="e8411-155">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="e8411-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="e8411-156">Clique na guia **Geral**.</span><span class="sxs-lookup"><span data-stu-id="e8411-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="e8411-157">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e8411-157">Click **Add**.</span></span>

4.  <span data-ttu-id="e8411-p106">Digite o alias do servidor na caixa **Alias de servidor**. Na caixa **Bibliotecas de rede**, clique em **TCP/IP**. Na caixa **Nome do computador**, digite o nome do computador que atende os clientes de Soquetes TCP/IP. Na caixa **Número da porta**, digite a porta na qual o SQL Server atende.</span><span class="sxs-lookup"><span data-stu-id="e8411-p106">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="e8411-162">Clique em **OK** e, em seguida, em **OK** novamente para sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="e8411-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

