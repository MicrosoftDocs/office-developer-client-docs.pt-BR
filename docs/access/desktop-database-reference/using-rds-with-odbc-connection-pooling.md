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
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="71427-102">Utilizando o RDS com o pool de conexão ODBC</span><span class="sxs-lookup"><span data-stu-id="71427-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="71427-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="71427-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="71427-p101">Se você estiver usando uma fonte de dados ODBC, poderá utilizar a opção de pool de conexão no IIS (Internet Information Services, Serviços de Informação de Internet) para alcançar alto desempenho ao manipular a carga do cliente. O pool de conexão é um gerenciador de recursos para conexões, mantendo o estado aberto em conexões utilizadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="71427-p101">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load. Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="71427-106">Para ativar o pooling de conexão, consulte a documentação do IIS.</span><span class="sxs-lookup"><span data-stu-id="71427-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="71427-107"><<<<<<< Cabeça por favor, observe que ativar o pooling de conexão pode sujeitar o servidor Web a outras restrições, conforme indicado na documentação do Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="71427-107"><<<<<<< HEAD Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
<span data-ttu-id="71427-108">=== Observe que ativar o pooling de conexão pode sujeitar o servidor web a outras restrições, conforme indicado na documentação do Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="71427-108">======= Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
>>>>>>> <span data-ttu-id="71427-109">mestre</span><span class="sxs-lookup"><span data-stu-id="71427-109">master</span></span>

<span data-ttu-id="71427-110">Para garantir que o pooling de conexão seja estável e forneça ganho adicionais de desempenho, você deve configurar o Microsoft SQL Server para utilizar a biblioteca de rede de Soquete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-110">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="71427-111">Para fazer isso, você precisa:</span><span class="sxs-lookup"><span data-stu-id="71427-111">To do this, you need to:</span></span>

  - <span data-ttu-id="71427-112">Configurar o computador SQL Server para usar Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-112">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

<span data-ttu-id="71427-113"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="71427-113"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="71427-114">Configurar o servidor Web para usar Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-114">Configure the Web server to use TCP/IP Sockets.</span></span>
=======
  - <span data-ttu-id="71427-115">Configure o servidor web para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-115">Configure the web server to use TCP/IP Sockets.</span></span>
>>>>>>> <span data-ttu-id="71427-116">mestre</span><span class="sxs-lookup"><span data-stu-id="71427-116">master</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="71427-117">Configurando o computador SQL Server para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-117">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="71427-118">No computador SQL Server, execute o programa de configuração do SQL Server para que as interações com a fonte de dados utilizem a biblioteca de rede de Soquete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-118">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="71427-119">**Para especificar a biblioteca de rede de Soquete TCP/IP no computador SQL Server**</span><span class="sxs-lookup"><span data-stu-id="71427-119">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="71427-120">**No Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="71427-120">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="71427-121">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **Instalação SQL**.</span><span class="sxs-lookup"><span data-stu-id="71427-121">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="71427-122">Clique em **Continuar** duas vezes.</span><span class="sxs-lookup"><span data-stu-id="71427-122">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="71427-123">Na caixa de diálogo **Microsoft SQL Server  Opções**, selecione **Alterar suporte à rede** e, em seguida, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="71427-123">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="71427-124">Certifique-se de que a caixa de seleção **Soquetes TCP/IP** esteja marcada e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="71427-124">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="71427-125">Clique em **Continuar** para finalizar e sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="71427-125">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="71427-126">**No Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="71427-126">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="71427-127">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="71427-127">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="71427-128">Na guia **Geral** da caixa de diálogo, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="71427-128">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="71427-129">Na caixa de diálogo **Adicionar configuração da biblioteca de rede**, clique em **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="71427-129">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="71427-130">Nas caixas **Número da porta** e **Endereço de proxy**, digite o número da porta e o endereço de proxy fornecidos pelo administrador da rede.</span><span class="sxs-lookup"><span data-stu-id="71427-130">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="71427-131">Clique em **OK** para finalizar e sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="71427-131">Click **OK** to finish, and exit setup.</span></span>

<span data-ttu-id="71427-132"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="71427-132"><<<<<<< HEAD</span></span>
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="71427-133">Configurando o servidor Web para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-133">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="71427-p103">Há duas opções para configurar o servidor Web para usar soquetes TCP/IP. O que você faz depende de todos os SQL Servers serem acessados do servidor Web ou apenas de um SQL Server específico ser acessado do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="71427-p103">There are two options for configuring the Web server to use TCP/IP Sockets. What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="71427-p104">Se todos os SQL Servers forem acessados do servidor Web, será necessário executar o SQL Server Client Configuration Utility no computador do servidor Web. As seguintes etapas alteram a biblioteca de rede padrão para todas as conexões do SQL Server feitas desse servidor para usar a biblioteca de rede de Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-p104">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer. The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<a name="to-configure-the-web-server-all-sql-servers"></a><span data-ttu-id="71427-138">**Para configurar o servidor Web (todos os SQL Servers)**</span><span class="sxs-lookup"><span data-stu-id="71427-138">**To configure the Web server (all SQL Servers)**</span></span>
=======
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="71427-139">Configurando o servidor para usar soquetes de TCP/IP na web</span><span class="sxs-lookup"><span data-stu-id="71427-139">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="71427-140">Há duas opções para configurar o servidor web para usar soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-140">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="71427-141">O que fazer depende se todos os SQL Servers são acessados a partir do servidor web ou apenas um SQL Server específico é acessado a partir do servidor web.</span><span class="sxs-lookup"><span data-stu-id="71427-141">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="71427-142">Se todos os SQL Servers são acessados a partir do servidor web, você precisará executar o utilitário de configuração do cliente SQL Server no computador do servidor web.</span><span class="sxs-lookup"><span data-stu-id="71427-142">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="71427-143">As etapas a seguir alteram a biblioteca de rede padrão para todas as conexões do SQL Server feitas a partir deste servidor de web IIS para usar a biblioteca de rede soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-143">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="71427-144">**Para configurar o servidor web (todos os SQL Servers)**</span><span class="sxs-lookup"><span data-stu-id="71427-144">**To configure the web server (all SQL Servers)**</span></span>
>>>>>>> <span data-ttu-id="71427-145">mestre</span><span class="sxs-lookup"><span data-stu-id="71427-145">master</span></span>

<span data-ttu-id="71427-146">**Para Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="71427-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="71427-147">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="71427-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="71427-148">Clique na guia **Biblioteca de rede**.</span><span class="sxs-lookup"><span data-stu-id="71427-148">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="71427-149">Na caixa **Rede padrão**, selecione **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="71427-149">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="71427-150">Clique em **Concluído** para salvar as alterações e sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="71427-150">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="71427-151">**Para Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="71427-151">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="71427-152">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="71427-152">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="71427-153">Clique na guia **Geral**.</span><span class="sxs-lookup"><span data-stu-id="71427-153">Click the **General** tab.</span></span>

3.  <span data-ttu-id="71427-154">Na caixa **Biblioteca de rede padrão**, clique em **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="71427-154">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="71427-155">Clique em **OK** para salvar as alterações e sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="71427-155">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="71427-156"><<<<<<< Cabeça se um SQL Server específico é acessado a partir de um servidor Web, você precisará executar o utilitário de configuração do cliente SQL Server no computador do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="71427-156"><<<<<<< HEAD If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</span></span> <span data-ttu-id="71427-157">Para alterar a biblioteca de rede para uma conexão específica do SQL Server, configure o software SQL Server Client no computador do servidor Web como se segue.</span><span class="sxs-lookup"><span data-stu-id="71427-157">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<a name="to-configure-the-web-server-a-specific-sql-server"></a><span data-ttu-id="71427-158">**Para configurar o servidor Web (um SQL Server específico)**</span><span class="sxs-lookup"><span data-stu-id="71427-158">**To configure the Web server (a specific SQL Server)**</span></span>
=======
<span data-ttu-id="71427-159">Se um SQL Server específico é acessado a partir de um servidor web, você precisará executar o utilitário de configuração do cliente SQL Server no computador do servidor web.</span><span class="sxs-lookup"><span data-stu-id="71427-159">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="71427-160">Para alterar a biblioteca de rede para uma conexão do SQL Server específico, configure o software de cliente do SQL Server no computador do servidor web da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="71427-160">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="71427-161">**Para configurar o servidor web (um SQL Server específico)**</span><span class="sxs-lookup"><span data-stu-id="71427-161">**To configure the web server (a specific SQL Server)**</span></span>
>>>>>>> <span data-ttu-id="71427-162">mestre</span><span class="sxs-lookup"><span data-stu-id="71427-162">master</span></span>

<span data-ttu-id="71427-163">**Para Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="71427-163">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="71427-164">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 6.5** e, em seguida, clique em **SQL Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="71427-164">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="71427-165">Clique na guia **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="71427-165">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="71427-166">Na caixa **Servidor**, digite o nome do servidor para conexão utilizando **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="71427-166">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="71427-167">Na caixa **Nome DLL**, selecione **Soquetes TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="71427-167">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="71427-p109">Clique em **Adicionar/modificar**. Todas as fontes de dados apontando para esse servidor utilizarão Soquetes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="71427-p109">Click **Add/Modify**. All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="71427-170">Clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="71427-170">Click **Done**.</span></span>

<span data-ttu-id="71427-171">**Para Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="71427-171">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="71427-172">No menu **Iniciar**, aponte para **Programas**, aponte para **Microsoft SQL Server 7.0** e, em seguida, clique em **Client Configuration Utility**.</span><span class="sxs-lookup"><span data-stu-id="71427-172">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="71427-173">Clique na guia **Geral**.</span><span class="sxs-lookup"><span data-stu-id="71427-173">Click the **General** tab.</span></span>

3.  <span data-ttu-id="71427-174">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="71427-174">Click **Add**.</span></span>

4.  <span data-ttu-id="71427-p110">Digite o alias do servidor na caixa **Alias de servidor**. Na caixa **Bibliotecas de rede**, clique em **TCP/IP**. Na caixa **Nome do computador**, digite o nome do computador que atende os clientes de Soquetes TCP/IP. Na caixa **Número da porta**, digite a porta na qual o SQL Server atende.</span><span class="sxs-lookup"><span data-stu-id="71427-p110">Enter the alias of the server in the **Server alias** box. In the **Network libraries** box, click **TCP/IP**. In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients. In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="71427-179">Clique em **OK** e, em seguida, em **OK** novamente para sair do utilitário.</span><span class="sxs-lookup"><span data-stu-id="71427-179">Click **OK**, and then **OK** again to exit the utility.</span></span>

