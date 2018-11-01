---
title: Membros de Conexão (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d2c2af4dcf1cf8661d7cac170e8aa5b679ab083
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886916"
---
# <a name="connection-members-dao"></a><span data-ttu-id="00a14-102">Membros de Conexão (DAO)</span><span class="sxs-lookup"><span data-stu-id="00a14-102">Connection Members (DAO)</span></span>

<span data-ttu-id="00a14-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="00a14-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="00a14-104">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="00a14-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="00a14-105">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="00a14-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span> <span data-ttu-id="00a14-106">Um objeto Connection representa uma conexão com um banco de dados ODBC (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="00a14-106">A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>
 

## <a name="methods"></a><span data-ttu-id="00a14-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="00a14-107">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00a14-108">Nome</span><span class="sxs-lookup"><span data-stu-id="00a14-108">Name</span></span></p></th>
<th><p><span data-ttu-id="00a14-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="00a14-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00a14-110"><strong><a href="connection-cancel-method-dao.md">Cancelar</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="00a14-111">Cancela a execução de uma chamada assíncrona pendente do método (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="00a14-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00a14-112"><strong><a href="connection-close-method-dao.md">Fechar</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-113">Fecha um objeto <strong>Connection</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="00a14-113">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00a14-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-115">Cria um novo objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="00a14-115">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00a14-116"><strong><a href="connection-execute-method-dao.md">Execução</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-117">Executa uma consulta de ação ou executa uma instrução SQL no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="00a14-117">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00a14-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-119">Cria e anexa um novo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> à coleção <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="00a14-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="00a14-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="00a14-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00a14-121">Nome</span><span class="sxs-lookup"><span data-stu-id="00a14-121">Name</span></span></p></th>
<th><p><span data-ttu-id="00a14-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="00a14-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00a14-123"><strong><a href="connection-connect-property-dao.md">Conecte-se</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-p102">Define ou retorna um valor que fornece informações sobre a origem de uma conexão aberta. <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="00a14-p102">Sets or returns a value that provides information about the source of an open connection. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00a14-126"><strong><a href="connection-database-property-dao.md">Banco de dados</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="00a14-127">Retorna o objeto <strong><a href="database-object-dao.md">Database</a></strong> que corresponde a essa conexão (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="00a14-127">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00a14-128"><strong><a href="connection-name-property-dao.md">Nome</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-129">Retorna o nome de um <strong><a href="connection-object-dao.md">Connection</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="00a14-129">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00a14-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-p103">Retorna uma coleção <strong>QueryDefs</strong> que contém todos os objetos <strong>QueryDef</strong> da conexão especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="00a14-p103">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00a14-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-134">Define ou retorna um valor que especifica o número de segundos a serem aguardados antes de ocorrer um erro de tempo limite quando uma consulta é executada em uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="00a14-134">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00a14-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-136">Retorna o número de registros afetados pelo método <strong><a href="connection-execute-method-dao.md">Execute</a></strong> chamado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="00a14-136">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00a14-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-p104">Retorna uma coleção <strong>Recordsets</strong> que contém todos os recordsets abertos para a conexão especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="00a14-p104">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00a14-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="00a14-141">Indica se uma operação assíncrona ou não (ou seja, um método chamado com a opção <strong>dbRunAsync</strong>) concluiu a execução (somente em espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="00a14-141">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00a14-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-p105">Retorna um valor que indica se um objeto aceita transactions. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="00a14-p105">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00a14-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="00a14-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="00a14-p106">Retorna um valor que indica se você pode alterar o objeto DAO. <strong>Boolean</strong> somente leitura. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="00a14-p106">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

