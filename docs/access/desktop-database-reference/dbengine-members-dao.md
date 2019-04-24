---
title: Membros DBEngine (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294278"
---
# <a name="dbengine-members-dao"></a><span data-ttu-id="fa481-102">Membros DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="fa481-102">DBEngine members (DAO)</span></span>


<span data-ttu-id="fa481-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa481-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa481-104">O objeto DBEngine é de nível superior no modelo de objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="fa481-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="fa481-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa481-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa481-106">Nome</span><span class="sxs-lookup"><span data-stu-id="fa481-106">Name</span></span></p></th>
<th><p><span data-ttu-id="fa481-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa481-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa481-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-109">Inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="fa481-109">Begins a new transaction.</span></span> <span data-ttu-id="fa481-110"><strong>Database</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fa481-110">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-112">Encerra a transação atual e salva as alterações.</span><span class="sxs-lookup"><span data-stu-id="fa481-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-114">Copia e compacta um banco de dados fechado e oferece a opção de alterar sua versão, ordem de agrupamento e criptografia.</span><span class="sxs-lookup"><span data-stu-id="fa481-114">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="fa481-115">(Somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa481-115">(Microsoft Access workspaces only).</span></span> <span data-ttu-id="fa481-116">.</span><span class="sxs-lookup"><span data-stu-id="fa481-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-118">Cria um novo objeto <strong><a href="database-object-dao.md">Database</a></strong>, salva o banco de dados no disco e retorna um objeto <strong>Database</strong> aberto (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa481-118">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="fa481-119">.</span><span class="sxs-lookup"><span data-stu-id="fa481-119"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-121">Cria um novo objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="fa481-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-122"><strong><a href="dbengine-idle-method-dao.md">Estado</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-123">Suspende o processamento de dados, habilitando o mecanismo de banco de dados do Microsoft Access a concluir tarefas pendentes, como otimização de memória ou tempo limite da página (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa481-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-125">Um dos valores <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="fa481-125">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="fa481-126"><strong>Observação</strong>: os espaços de trabalho ODBCDirect não têm suporte no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="fa481-126"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="fa481-127">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fa481-127">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="fa481-128">Abre um objeto <strong><a href="connection-object-dao.md">Connection</a></strong> em uma fonte de dados ODBC (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="fa481-128">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-130">Abre um banco de dados especificado e retorna uma referência ao objeto <strong><a href="database-object-dao.md">Database</a></strong> que o representa.</span><span class="sxs-lookup"><span data-stu-id="fa481-130">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-p105">Insere as informações de conexão para uma fonte de dados ODBC no Registro do Windows. O driver ODBC precisa das informações de conexão quando a fonte de dados ODBC é aberta durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="fa481-p105">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-135">Encerra a transação atual e restaura os bancos de dados no objeto <strong>Workspace</strong> para o estado em que estavam quando a transação atual começou.</span><span class="sxs-lookup"><span data-stu-id="fa481-135">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-137">Substitui temporariamente os valores para as chaves do mecanismo de banco de dados do Microsoft Access no Registro do Windows (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa481-137">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="fa481-138">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa481-138">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa481-139">Nome</span><span class="sxs-lookup"><span data-stu-id="fa481-139">Name</span></span></p></th>
<th><p><span data-ttu-id="fa481-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa481-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa481-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-142">Define a senha utilizada para criar o <strong>Workspace</strong> padrão quando ele é inicializado.</span><span class="sxs-lookup"><span data-stu-id="fa481-142">Sets the password used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="fa481-143"><strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fa481-143">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-145">Define ou retorna um valor que indica o tipo de espaço de trabalho que será utilizado pelo próximo objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> criado.</span><span class="sxs-lookup"><span data-stu-id="fa481-145">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-147">Define o nome de usuário utilizado para criar o <strong>Workspace</strong> padrão quando ele é inicializado.</span><span class="sxs-lookup"><span data-stu-id="fa481-147">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="fa481-148"><strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fa481-148">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-149"><strong><a href="dbengine-errors-property-dao.md">Erros</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-149"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-150">Retorna uma coleção <strong>Errors</strong> que contém todos os objetos <strong>Error</strong> armazenados para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="fa481-150">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object.</span></span> <span data-ttu-id="fa481-151">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fa481-151">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-153">Define ou retorna informações sobre a chave do Registro do Windows que contém os valores do mecanismo do banco de dados do Microsoft Access (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa481-153">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-155">Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="fa481-155">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-156"><strong><a href="dbengine-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-156"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-157">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="fa481-157">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="fa481-158">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fa481-158">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa481-159"><strong><a href="dbengine-version-property-dao.md">Versão</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-159"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-160">Retorna a versão do DAO atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="fa481-160">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="fa481-161"><strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fa481-161">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa481-162"><strong><a href="dbengine-workspaces-property-dao.md">Workplaces</a></strong></span><span class="sxs-lookup"><span data-stu-id="fa481-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="fa481-163">Retorna uma coleção <strong>Workspaces</strong> que contém todos os objetos <strong>Workspace</strong> ativos e não ocultos.</span><span class="sxs-lookup"><span data-stu-id="fa481-163">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects.</span></span> <span data-ttu-id="fa481-164">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fa481-164">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

