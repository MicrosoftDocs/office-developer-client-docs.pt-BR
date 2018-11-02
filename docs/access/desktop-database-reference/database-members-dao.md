---
title: Membros do banco de dados (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b75fff8251e74a525798cd5eb2c6feb2d69016b7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919749"
---
# <a name="database-members-dao"></a><span data-ttu-id="610dd-102">Membros do banco de dados (DAO)</span><span class="sxs-lookup"><span data-stu-id="610dd-102">Database members (DAO)</span></span>


<span data-ttu-id="610dd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="610dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="610dd-104">Um objeto Database representa um banco de dados aberto.</span><span class="sxs-lookup"><span data-stu-id="610dd-104">A Database object represents an open database.</span></span>

## <a name="methods"></a><span data-ttu-id="610dd-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="610dd-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="610dd-106">Nome</span><span class="sxs-lookup"><span data-stu-id="610dd-106">Name</span></span></p></th>
<th><p><span data-ttu-id="610dd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="610dd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="610dd-108"><strong><a href="database-close-method-dao.md">Fechar</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-108"><strong><a href="database-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-109">Fecha um objeto <strong>Database</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="610dd-109">Closes an open <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-110"><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-110"><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p101">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="610dd-p101">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-113"><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-113"><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-114">Cria um novo objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="610dd-114">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-115"><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-115"><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p102">Cria um novo objeto <strong><a href="relation-object-dao.md">Relation</a></strong> (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="610dd-p102">Creates a new <strong><a href="relation-object-dao.md">Relation</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-118"><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-118"><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p103">Cria um novo objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong> (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="610dd-p103">Creates a new <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-121"><strong><a href="database-execute-method-dao.md">Execução</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-121"><strong><a href="database-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-122">Executa uma consulta de ação ou executa uma instrução SQL no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="610dd-122">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-123"><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-123"><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-124">Cria uma nova réplica a partir de uma outra réplica do banco de dados (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="610dd-124">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-125"><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-125"><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-126">Altera a senha de um banco de dados existente do mecanismo de banco de dados do Microsoft Access (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="610dd-126">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-127"><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-127"><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-128">Cria e anexa um novo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> à coleção <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="610dd-128">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-129"><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-129"><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p104">Sincroniza as alterações em uma réplica parcial com a réplica completa, limpa todos os registros na réplica parcial e preenche novamente a réplica parcial com base nos filtros da réplica atual. (Apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="610dd-p104">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters. (Microsoft Access database engine databases only.).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-132"><strong><a href="database-synchronize-method-dao.md">Sincronizar</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-132"><strong><a href="database-synchronize-method-dao.md">Synchronize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p105">Sincroniza duas réplicas. (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="610dd-p105">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="610dd-135">Propriedades</span><span class="sxs-lookup"><span data-stu-id="610dd-135">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="610dd-136">Nome</span><span class="sxs-lookup"><span data-stu-id="610dd-136">Name</span></span></p></th>
<th><p><span data-ttu-id="610dd-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="610dd-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="610dd-138"><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-138"><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p106">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). <strong>Long</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p106">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-141"><strong><a href="database-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-141"><strong><a href="database-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p107">Define ou retorna um valor que fornece informações sobre a origem de um banco de dados aberto. <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="610dd-p107">Sets or returns a value that provides information about the source an open database. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-144"><strong><a href="database-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-144"><strong><a href="database-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="610dd-p108">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="610dd-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="610dd-147">Retorna o objeto <strong><a href="connection-object-dao.md">Connection</a></strong> que corresponde ao banco de dados (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="610dd-147">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-148"><strong><a href="database-containers-property-dao.md">Containers</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-148"><strong><a href="database-containers-property-dao.md">Containers</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p109">Retorna uma coleção <strong>Containers</strong> que representa todos os objetos <strong>Container</strong> no banco de dados especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p109">Returns a <strong>Containers</strong> collection that represents all of the <strong>Container</strong> objects in the specifed database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-151"><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-151"><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-152">Define ou retorna um valor de 16 bytes que identifica exclusivamente a Design Mestre em um conjunto de réplicas (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="610dd-152">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-153"><strong><a href="database-name-property-dao.md">Nome</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-153"><strong><a href="database-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p110">Retorna o nome do objeto especificado. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p110">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-156"><strong><a href="database-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-156"><strong><a href="database-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p111">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-159"><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-159"><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p112">Retorna uma coleção <strong>QueryDefs</strong> que contém todos os objetos <strong>QueryDef</strong> do banco de dados especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p112">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-162"><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-162"><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-163">Define ou retorna um valor que especifica o número de segundos a serem aguardados antes de ocorrer um erro de tempo limite quando uma consulta é executada em uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="610dd-163">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-164"><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-164"><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-165">Retorna o número de registros afetados pelo método <strong><a href="connection-execute-method-dao.md">Execute</a></strong> chamado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="610dd-165">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-166"><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-166"><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p113">Retorna uma coleção <strong>Recordsets</strong> que contém todos os recordsets abertos para o banco de dados especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p113">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-169"><strong><a href="database-relations-property-dao.md">Relations</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-169"><strong><a href="database-relations-property-dao.md">Relations</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p114">Retorna uma coleção <strong>Relations</strong> que contém todos os objetos <strong>Relation</strong> armazenados para o banco de dados especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p114">Returns a <strong>Relations</strong> collection that contains all of the stored <strong>Relation</strong> objects for the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-172"><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-172"><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-173">Retorna um valor de 16 bytes que identifica exclusivamente uma réplica de um banco dados (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="610dd-173">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-174"><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-174"><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p115">Retorna uma coleção <strong>TableDefs</strong> que contém todos os objetos <strong>TableDef</strong> armazenados no banco de dados especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p115">Returns a <strong>TableDefs</strong> collection that contains all of the <strong>TableDef</strong> objects stored in the specified database. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-177"><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-177"><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p116">Retorna um valor que indica se um objeto aceita transactions. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p116">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="610dd-180"><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-180"><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p117">Retorna um valor que indica se você pode alterar um objeto DAO. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p117">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="610dd-183"><strong><a href="database-version-property-dao.md">Versão</a></strong></span><span class="sxs-lookup"><span data-stu-id="610dd-183"><strong><a href="database-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="610dd-p118">Em um espaço de trabalho do Microsoft Access , retorna a versão do mecanismo de banco de dados do Microsoft Jet ou do Microsoft Access que criou o banco de dados. <strong>String</strong> de somente leitura.</span><span class="sxs-lookup"><span data-stu-id="610dd-p118">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

