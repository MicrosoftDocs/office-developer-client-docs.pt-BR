---
title: Membros de QueryDef (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84f8be8360996eb209462347dc18b118cf460442
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937614"
---
# <a name="querydef-members-dao"></a><span data-ttu-id="889fa-102">Membros de QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="889fa-102">QueryDef members (DAO)</span></span>


<span data-ttu-id="889fa-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="889fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="889fa-104">Um objeto QueryDef é uma definição armazenada de uma consulta em um banco de dados do mecanismo de banco de dados do Microsoft Access ou uma definição temporária de uma consulta em um espaço de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="889fa-104">A QueryDef object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="methods"></a><span data-ttu-id="889fa-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="889fa-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="889fa-106">Nome</span><span class="sxs-lookup"><span data-stu-id="889fa-106">Name</span></span></p></th>
<th><p><span data-ttu-id="889fa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="889fa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="889fa-108"><strong><a href="querydef-cancel-method-dao.md">Cancelar</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="889fa-p101">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="889fa-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="889fa-111">Cancela a execução de uma chamada assíncrona pendente do método (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="889fa-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-112"><strong><a href="querydef-close-method-dao.md">Fechar</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-112"><strong><a href="querydef-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-113">Fecha um objeto <strong>QueryDef</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="889fa-113">Closes an open <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-115">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="889fa-115">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-116"><strong><a href="querydef-execute-method-dao.md">Execução</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-117">Executa uma instrução SQL no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="889fa-117">Executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-119">Cria e anexa um novo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> à coleção <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="889fa-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="889fa-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="889fa-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="889fa-121">Nome</span><span class="sxs-lookup"><span data-stu-id="889fa-121">Name</span></span></p></th>
<th><p><span data-ttu-id="889fa-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="889fa-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="889fa-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p102">Define ou retorna o número de registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente. <strong>Long</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="889fa-p102">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p103">Define ou retorna um valor que fornece as informações sobre a fonte do banco de dados usada em uma consulta passagem. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="889fa-p103">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p104">Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). <strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="889fa-p104">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p105">Retorna uma coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> que representa todos os objetos <strong><a href="field-object-dao.md">Field</a></strong> armazenados para o objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="889fa-p105">Returns a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection that represents all stored <strong><a href="field-object-dao.md">Field</a></strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p106">Retorna a data e a hora da alteração feita mais recentemente em um objeto. <strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="889fa-p106">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-139">Define ou retorna o número máximo de registros a serem retornados de uma consulta em relação à fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="889fa-139">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-140"><strong><a href="querydef-name-property-dao.md">Nome</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p107">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="889fa-p107">Returns or sets the name of the specified object. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-144">Indica se o número de segundos a ser aguardado antes da ocorrência de um erro de tempo limite durante a execução de <strong><a href="querydef-object-dao.md">QueryDef</a></strong> em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="889fa-144">Indicates the number of seconds to wait before a timeout error occurs when a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> is executed on an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-145"><strong><a href="querydef-parameters-property-dao.md">Parâmetros</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-145"><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p108">Retorna uma coleção <strong><a href="parameters-collection-dao.md">Parameters</a></strong> que contém todos os objetos <strong><a href="parameter-object-dao.md">Parameter</a></strong> do <strong>QueryDef</strong> especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="889fa-p108">Returns a <strong><a href="parameters-collection-dao.md">Parameters</a></strong> collection that contains all of the <strong><a href="parameter-object-dao.md">Parameter</a></strong> objects of the specified <strong>QueryDef</strong>. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="889fa-p109">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="889fa-p109">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="889fa-p110">Define ou retorna um valor que indica se a consulta está preparada no servidor como um procedimento armazenado temporariamente usando a função API <strong>SQLPrepare</strong> do ODBC, antes da execução ou executar apenas usando a função API <strong>SQLExecDirect</strong> do ODBC (apenas espaços de trabalho ODBCDirect). <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong> de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="889fa-p110">Sets or returns a value that indicates whether the query should be prepared on the server as a temporary stored procedure, using the ODBC <strong>SQLPrepare</strong> API function, prior to execution, or just executed using the ODBC <strong>SQLExecDirect</strong> API function (ODBCDirect workspaces only). Read/Write <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-153"><strong><a href="querydef-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p111">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="889fa-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-157">Retorna o número de registros afetados pelo método <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> chamado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="889fa-157">Returns the number of records affected by the most recently invoked <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-159">Define ou retorna um valor que indica se uma consulta passagem SQL para um banco de dados externo retornará registros (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="889fa-159">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-161">Define ou retorna a instrução SQL que define a consulta executada por um objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="889fa-161">Sets or returns the SQL statement that defines the query executed by a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="889fa-p112">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="889fa-p112">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="889fa-165">Indica se uma operação assíncrona ou não (ou seja, um método chamado com a opção <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>) concluiu a execução (somente em espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="889fa-165">Indicates whether or not an asynchronous operation (that is, a method called with the <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="889fa-166"><strong><a href="querydef-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-167">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="889fa-167">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="889fa-168">Somente leitura<strong>inteiro</strong>.</span><span class="sxs-lookup"><span data-stu-id="889fa-168">Read-only<strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="889fa-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="889fa-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="889fa-p114">Retorna um valor que indica se você pode alterar um objeto DAO. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="889fa-p114">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

