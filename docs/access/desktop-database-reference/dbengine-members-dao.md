---
title: Membros de DBEngine (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2763825fa3e182d2007be65a88e18988699f26f8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891156"
---
# <a name="dbengine-members-dao"></a><span data-ttu-id="28326-102">Membros de DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="28326-102">DBEngine Members (DAO)</span></span>


<span data-ttu-id="28326-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="28326-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28326-104">O objeto DBEngine é de nível superior no modelo de objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="28326-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="28326-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="28326-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28326-106">Nome</span><span class="sxs-lookup"><span data-stu-id="28326-106">Name</span></span></p></th>
<th><p><span data-ttu-id="28326-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="28326-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28326-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p101">Inicia uma nova transação. <strong>Database</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="28326-p101">Begins a new transaction. Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-112">Encerra a transação atual e salva as alterações.</span><span class="sxs-lookup"><span data-stu-id="28326-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p102">Copia e compacta um banco de dados fechado e dá a você a opção de alterar sua versão, ordem de agrupamento e criptografia. (espaços de trabalho do Microsoft Access apenas).</span><span class="sxs-lookup"><span data-stu-id="28326-p102">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption. (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-117"><strong><a href="dbengine-createdatabase-method-dao.md">Método CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p103">Cria um novo objeto <strong><a href="database-object-dao.md">Database</a></strong>, salva o banco de dados no disco e retorna um objeto <strong>Database</strong> aberto (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="28326-p103">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-121">Cria um novo objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="28326-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-122"><strong><a href="dbengine-idle-method-dao.md">Ocioso</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-123">Suspende o processamento de dados, habilitando o mecanismo de banco de dados do Microsoft Access a concluir tarefas pendentes, como otimização de memória ou tempo limite da página (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="28326-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="28326-p104">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="28326-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="28326-127">Abre um objeto <strong><a href="connection-object-dao.md">Connection</a></strong> em uma fonte de dados ODBC (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="28326-127">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-128"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-128"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-129">Abre um banco de dados especificado e retorna uma referência ao objeto <strong><a href="database-object-dao.md">Database</a></strong> que o representa.</span><span class="sxs-lookup"><span data-stu-id="28326-129">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-130"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-130"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p105">Insere as informações de conexão para uma fonte de dados ODBC no Registro do Windows. O driver ODBC precisa das informações de conexão quando a fonte de dados ODBC é aberta durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="28326-p105">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-133"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-133"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-134">Encerra a transação atual e restaura os bancos de dados no objeto <strong>Workspace</strong> para o estado em que estavam quando a transação atual começou.</span><span class="sxs-lookup"><span data-stu-id="28326-134">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-135"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-135"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-136">Substitui temporariamente os valores para as chaves do mecanismo de banco de dados do Microsoft Access no Registro do Windows (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="28326-136">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="28326-137">Propriedades</span><span class="sxs-lookup"><span data-stu-id="28326-137">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28326-138">Nome</span><span class="sxs-lookup"><span data-stu-id="28326-138">Name</span></span></p></th>
<th><p><span data-ttu-id="28326-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="28326-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28326-140"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-140"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p106">Define a senha utilizada para criar o <strong>Workspace</strong> padrão quando ele é inicializado. <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="28326-p106">Sets the password used to create the default <strong>Workspace</strong> when it is initialized. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-143"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-143"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-144">Define ou retorna um valor que indica o tipo de espaço de trabalho que será utilizado pelo próximo objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> criado.</span><span class="sxs-lookup"><span data-stu-id="28326-144">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-145"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-145"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p107">Define o nome de usuário utilizado para criar o <strong>Workspace</strong> padrão quando ele é inicializado. <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="28326-p107">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-148"><strong><a href="dbengine-errors-property-dao.md">Erros</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-148"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p108">Retorna uma coleção <strong>Errors</strong> que contém todos os objetos <strong>Error</strong> armazenados para o objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="28326-p108">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-151"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-151"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-152">Define ou retorna informações sobre a chave do Registro do Windows que contém os valores do mecanismo do banco de dados do Microsoft Access (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="28326-152">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-153"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-153"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-154">Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="28326-154">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-155"><strong><a href="dbengine-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-155"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p109">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="28326-p109">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28326-158"><strong><a href="dbengine-version-property-dao.md">Versão</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-158"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p110">Retorna a versão do DAO atualmente em uso. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="28326-p110">Rreturns the version of DAO currently in use. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28326-161"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span><span class="sxs-lookup"><span data-stu-id="28326-161"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="28326-p111">Retorna uma coleção <strong>Workspaces</strong> que contém todos os objetos <strong>Workspace</strong> ativos e não ocultos. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="28326-p111">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects. Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

