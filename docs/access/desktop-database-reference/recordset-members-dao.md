---
title: Membros do Conjunto de Registros (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c36187eef0b55681b2ba426d979f42ee8a6efea8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284803"
---
# <a name="recordset-members-dao"></a><span data-ttu-id="8f5bd-102">Membros do Conjunto de Registros (DAO)</span><span class="sxs-lookup"><span data-stu-id="8f5bd-102">Recordset members (DAO)</span></span>


<span data-ttu-id="8f5bd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f5bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f5bd-104">Um objeto Recordset representa os registros em uma tabela base ou os registros resultantes da execução de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-104">A Recordset object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="8f5bd-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="8f5bd-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f5bd-106">Nome</span><span class="sxs-lookup"><span data-stu-id="8f5bd-106">Name</span></span></p></th>
<th><p><span data-ttu-id="8f5bd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f5bd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-108"><a href="recordset-addnew-method-dao.md">expression</a>  . <strong>AddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-109">Cria um novo registro para um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-109">Creates a new record for an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-111"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-111">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-113">Cancela a execução de uma chamada assíncrona pendente do método (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-115">Cancela qualquer atualizações pendentes de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-117">Cria um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> duplicado que se refere ao objeto <strong>Recordset</strong> original.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-119">Fecha um <strong>Recordset</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-120"><a href="recordset-copyquerydef-method-dao.md">expression</a>  . <strong>CopyQueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-121">Retorna um objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong> que é uma cópia do <strong>QueryDef</strong> utilizado para criar o objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> representado pelo espaço reservado do conjunto de registros (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="8f5bd-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the  recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8f5bd-122">.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-124">Não é suportado por este objeto.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-126">Copia o registro atual de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável para o buffer de cópia para edição subsequente.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-128">Preenche todo ou uma parte do cache local para um objeto <strong>Recordset</strong> que contém dados de uma fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access (apenas bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-130">Localiza o primeiro registro em um dynaset ou objeto de tipo instantâneo do <strong>Conjunto de registros</strong>, que atende aos critérios específicos e torna esse registro atual (somente para espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-132">Localiza o último registro em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (Apenas Espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-p103">Localiza o próximo registro em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ). .</span><span class="sxs-lookup"><span data-stu-id="8f5bd-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-p104">Localiza o registro anterior em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access). .</span><span class="sxs-lookup"><span data-stu-id="8f5bd-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-140">Recupera múltiplas linhas de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-142">Move a posição do registro atual em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-143"><a href="recordset-movefirst-method-dao.md">expression</a>  . <strong>MoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-144">Move para o primeiro registro em um objeto <strong>Recordset</strong> específico e o torna o registro atual. </span><span class="sxs-lookup"><span data-stu-id="8f5bd-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-146">Move para o último registro em um objeto <strong>Recordset</strong> específico e o torna o registro atual. </span><span class="sxs-lookup"><span data-stu-id="8f5bd-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-147"><a href="recordset-movenext-method-dao.md">expression</a>  . <strong>MoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-148">Move para o próximo registro em um objeto <strong>Recordset</strong> específico e o torna o registro atual. </span><span class="sxs-lookup"><span data-stu-id="8f5bd-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-149"><a href="recordset-moveprevious-method-dao.md">expression</a>  . <strong>MovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-150">Move para o registro anterior em um objeto <strong>Recordset</strong> específico e o torna o registro atual. </span><span class="sxs-lookup"><span data-stu-id="8f5bd-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-151"><a href="recordset-nextrecordset-method-dao.md">expression</a>  . <strong>NextRecordset</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-152"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-152">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-153">Use o ADO caso queira acessar fontes de banco de dados externo sem utilizar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-154">Obtém o próximo conjunto de registros, se houver, retornado por uma consulta seleção de várias partes em uma chamada <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong>, e retorna um valor <strong>Boolean</strong> indicando se um ou mais registros adicionais estão pendentes (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-156">Cria um novo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> e o acrescenta à coleção <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-158">Atualiza os dados no objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> reexecutando a consulta na qual o objeto é baseado.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-159"><strong><a href="recordset-seek-method-dao.md">Buscar</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-160">Localiza o registro em um objeto <strong>Recordset</strong> do tipo tabela indexada que satisfaz os critérios especificados para o índice atual e torna esse registro o registro atual (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-161"><strong><a href="recordset-update-method-dao.md">Atualizar</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-162"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-162">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-163">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-164">Salva o conteúdo do buffer de cópia em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="8f5bd-165">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f5bd-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f5bd-166">Nome</span><span class="sxs-lookup"><span data-stu-id="8f5bd-166">Name</span></span></p></th>
<th><p><span data-ttu-id="8f5bd-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f5bd-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-168"><a href="recordset-absoluteposition-property-dao.md">expression</a>  . <strong>AbsolutePosition</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-169">Define ou retorna o número de registro relativo do registro atual de um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-169">Sets or returns the relative record number of a <strong>Recordset2</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-170"><a href="recordset-batchcollisioncount-property-dao.md">expression</a>  . <strong>BatchCollisionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-171"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-171">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-172">Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-173">Retorna o número de registros que não concluíram a última atualização em lotes (somente em espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-174"><a href="recordset-batchcollisions-property-dao.md">expression</a>  . <strong>BatchCollisions</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-175"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-175">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-176">Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-177">Retorna uma matriz de indicadores mostrando as linhas que geraram colisões na última operação de atualização em lotes (somente em espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-178"><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-178"><a href="recordset-batchsize-property-dao.md">expression</a>  . <strong>BatchSize</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-179"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-179">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-180">Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-181">Defina ou retorna o número de instruções enviadas de volta para o servidor em cada lote (somente nos espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-183">Retorna um valor que indica se a posição atual do registro será antes do primeiro registro em um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="8f5bd-184"><strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-186">Define ou retorna um marcador que identifica exclusivamente o registro atual in em objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-188">Retorna um valor que indica se um objeto <strong>Recordset</strong> suporta marcadores, que pode ser definido usando a propriedade <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-189"><a href="recordset-cachesize-property-dao.md">expression</a>  . <strong>CacheSize</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-190">Define ou retorna vários registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="8f5bd-191"><strong>Long</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-192">CacheStart Property</span></span></p></td>
<td><p><span data-ttu-id="8f5bd-193">Define ou retorna um valor que especifica o marcador do primeiro registro em um objeto Recordset do tipo dynaset, que contém os dados a serem armazenados localmente a partir de uma fonte de dados ODBC (somente em espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-195">Retorna o objeto <strong><a href="connection-object-dao.md">Connection</a></strong> que corresponde ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-197">Retorna a data e a hora na qual a tabela base foi criada (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-197">Returns the date and time a base table was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8f5bd-198">Somente leitura <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-199"><a href="recordset-editmode-property-dao.md">expression</a>  . <strong>EditMode</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-200">Retorna um valor que indica o estado da edição do registro atual.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-202">Retorna um valor que indica se a posição do registro atual será depois do último registro em um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="8f5bd-203"><strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-205">Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-205">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="8f5bd-206">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-206">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-208">Define ou retorna um valor que determina os registros incluídos em um objeto <strong>Recordset</strong> aberto posteriormente (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8f5bd-209"><strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-211">Define ou retorna um valor que indica o nome do objeto <strong><a href="index-object-dao.md">Index</a></strong> atual em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> do tipo Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="8f5bd-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-212">LastModified Property</span></span></p></td>
<td><p><span data-ttu-id="8f5bd-213">Retorna um marcador indicando o registro mais recentemente adicionado ou alterado.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-214">LastUpdated Property</span></span></p></td>
<td><p><span data-ttu-id="8f5bd-215">Retorna a data e a hora da alteração mais recente feita em uma tabela base.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-215">Returns the date and time of the most recent change made to a base table.</span></span> <span data-ttu-id="8f5bd-216">Somente leitura <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-217"><a href="recordset-lockedits-property-dao.md">expression</a>  . <strong>LockEdits</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-218">Define ou retorna um valor indicando o tipo de bloqueio que está em vigor durante a edição.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-220">Retorna o nome do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-220">Returns the name of the specified object.</span></span> <span data-ttu-id="8f5bd-221"><strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-222"><a href="recordset-nomatch-property-dao.md">expression</a>  . <strong>NoMatch</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-223">Indica se um registro em particular foi localizado usando o método <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> ou um dos métodos <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="8f5bd-223">Indicates whether a particular record was found by using the <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-224">PercentPosition Property</span></span></p></td>
<td><p><span data-ttu-id="8f5bd-225">Define ou retorna um valor que indica o local aproximado do registro atual no objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> com base em uma porcentagem de registros no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-225">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-227">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-227">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="8f5bd-228">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-228">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-p119">Retorna o número de registros acessados em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> ou o número total de registros em um objeto <strong>Recordset</strong> do tipo tabela ou do objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. <strong>Long</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-p119">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-233"><a href="recordset-recordstatus-property-dao.md">expression</a>  . <strong>RecordStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-234"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-234">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-235">Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-235">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-p121">Retorna um valor que indica o status de atualização do registro atual se este fizer parte de uma atualização em lotes (somente em espaços de trabalho do ODBCDirect). <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-p121">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-239">Retorna um valor que indica se um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> oferece suporte ao método <strong><a href="recordset-requery-method-dao.md">Requery</a></strong>, que reexecuta a consulta na qual está baseado o objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-239">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-241">Define ou retorna a ordem de classificação dos registros em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> (somente em espaços de trabalho do Microsoft Access) </span><span class="sxs-lookup"><span data-stu-id="8f5bd-241">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-242"><a href="recordset-stillexecuting-property-dao.md">expression</a>  . <strong>StillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-243"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-243">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-244">Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-244">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-245">Indica se uma operação assíncrona ou não (ou seja, um método chamado com a opção <strong>dbRunAsync</strong>) concluiu a execução (somente em espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8f5bd-245">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-247">Retorna um valor que indica se um objeto tem suporte em transações.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-247">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="8f5bd-248"><strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-248">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-249"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-249"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-250">A descrição deste membro aparecerá na versão final do Office 14.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-250">The description for this member will appear in the final release of Office 14.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-252">Retorna um valor que indica se você pode alterar um objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-252">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="8f5bd-253"><strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-253">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-255"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-255">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8f5bd-256">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-256">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="8f5bd-p126">Define ou retorna um valor que indica como a cláusula WHERE será construída para cada registro durante uma atualização em lotes e se a atualização em lotes deverá usar uma instrução UPDATE ou DELETE seguida de INSERT (somente em espaços de trabalho ODBCDirect). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8f5bd-p126">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f5bd-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-260">Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-260">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f5bd-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="8f5bd-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="8f5bd-p127">Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto <strong>Field</strong> não satisfaça a regra de validação especificada pela definição da propriedade <strong>ValidationRule</strong> (somente nos espaços de trabalho do Microsoft Access). <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8f5bd-p127">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

