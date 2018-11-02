---
title: Membros do espaço de trabalho (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3deb259e5058fe595099e5fa556ff5fca8e4baf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923886"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="bddbf-102">Membros do espaço de trabalho (DAO)</span><span class="sxs-lookup"><span data-stu-id="bddbf-102">Workspace members (DAO)</span></span>


<span data-ttu-id="bddbf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bddbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bddbf-p101">Um objeto Workspace define uma sessão nomeada por um usuário. Ele contém bancos de dados abertos e fornece mecanismos para transações simultâneas e, nos espaços de trabalho do Microsoft Access, suporte a grupos de trabalho seguros.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p101">A Workspace object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="bddbf-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="bddbf-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bddbf-107">Nome</span><span class="sxs-lookup"><span data-stu-id="bddbf-107">Name</span></span></p></th>
<th><p><span data-ttu-id="bddbf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bddbf-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-p102">Inicia uma nova transação. <strong>Database</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p102">Begins a new transaction. Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bddbf-112"><strong><a href="workspace-close-method-dao.md">Fechar</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-113">Fecha um <strong>Workspace</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="bddbf-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-115">Encerra a transação atual e salva as alterações.</span><span class="sxs-lookup"><span data-stu-id="bddbf-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bddbf-116"><strong><a href="workspace-createdatabase-method-dao.md">Método CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-117">Cria um novo objeto <strong><a href="database-object-dao.md">Database</a></strong>, salva o banco de dados no disco e retorna um objeto <strong>Database</strong> aberto (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bddbf-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="bddbf-p103">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="bddbf-121">Abre um objeto <strong><a href="connection-object-dao.md">Connection</a></strong> em uma fonte de dados ODBC (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bddbf-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bddbf-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-123">Abre um banco de dados especificado em um objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> e retorna uma referência ao objeto <strong><a href="database-object-dao.md">Database</a></strong> que o representa.</span><span class="sxs-lookup"><span data-stu-id="bddbf-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-125">Encerra a transação atual e restaura os bancos de dados no objeto <strong>Workspace</strong> para o estado em que estavam quando a transação atual começou.</span><span class="sxs-lookup"><span data-stu-id="bddbf-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="bddbf-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bddbf-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bddbf-127">Nome</span><span class="sxs-lookup"><span data-stu-id="bddbf-127">Name</span></span></p></th>
<th><p><span data-ttu-id="bddbf-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="bddbf-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-p104">Retorna uma coleção <strong>Connections</strong> que representa as conexões atuais do <strong>Workspace</strong> especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p104">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bddbf-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-p105">Retorna uma coleção <strong>Databases</strong> que representa os banco de dados abertos em um <strong>Workspace</strong> especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p105">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="bddbf-p106">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="bddbf-138">Define ou retorna o tipo de driver de cursor utilizado na conexão criada pelos métodos <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> ou <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bddbf-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bddbf-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-140">Define ou retorna um valor que indica se vários transactiond, que envolvem o mesmo mecanismo do banco de dados do Microsoft Access conectado à fonte de dados ODBC, estão isolados (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bddbf-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-142">Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="bddbf-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bddbf-143"><strong><a href="workspace-name-property-dao.md">Nome</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-p107">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bddbf-147"><strong><a href="workspace-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-p108">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p108">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bddbf-150"><strong><a href="workspace-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="bddbf-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bddbf-p109">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>Integer</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="bddbf-p109">Sets or returns a value that indicates the operational type or data type of an object. Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

