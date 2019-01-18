---
title: Membros do Recordset2 (DAO)
TOCTitle: Recordset2 Members
ms:assetid: 6ef57191-9da4-7904-d55c-60b59b895a50
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195572(v=office.15)
ms:contentKeyID: 48545523
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29d1472e8cd02d8968ba84dbc1c1cf99be7ee858
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726278"
---
# <a name="recordset2-members-dao"></a><span data-ttu-id="85d10-102">Membros do Recordset2 (DAO)</span><span class="sxs-lookup"><span data-stu-id="85d10-102">Recordset2 members (DAO)</span></span>


<span data-ttu-id="85d10-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="85d10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85d10-104">Um objeto Recordset2 representa os registros em uma tabela de base ou os registros resultantes da execução de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="85d10-104">A Recordset2 object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="85d10-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="85d10-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85d10-106">Nome</span><span class="sxs-lookup"><span data-stu-id="85d10-106">Name</span></span></p></th>
<th><p><span data-ttu-id="85d10-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="85d10-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85d10-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-109">Cria um novo registro para um objeto <strong>Recordset2</strong> atualizável.</span><span class="sxs-lookup"><span data-stu-id="85d10-109">Creates a new record for an updatable <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-110"><strong><a href="recordset2-cancel-method-dao.md">Cancelar</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-110"><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-111"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-111"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-112">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-113">Cancela a execução de uma chamada assíncrona pendente do método (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="85d10-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-115">Cancela quaisquer atualizações pendentes para um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-117">Cria um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> duplicado que faz referência ao objeto <strong>Recordset2</strong> original.</span><span class="sxs-lookup"><span data-stu-id="85d10-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-118"><strong><a href="recordset2-close-method-dao.md">Fechar</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-118"><strong><a href="recordset2-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-119">Fecha um <strong>Recordset</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="85d10-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-121">Retorna um objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong> que é uma cópia do <strong>QueryDef</strong> usado para criar o objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> representado por um espaço reservado recordset (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="85d10-122">.</span><span class="sxs-lookup"><span data-stu-id="85d10-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-123"><strong><a href="recordset2-delete-method-dao.md">Excluir</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-124">Não aceito para este objeto.</span><span class="sxs-lookup"><span data-stu-id="85d10-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-126">Copia o registro atual de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável para o buffer de cópia para edição subsequente.</span><span class="sxs-lookup"><span data-stu-id="85d10-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-128">Preenche parcial ou totalmente um cache local de um objeto <strong>Recordset</strong> que contém dados de uma fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access (somente bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-130">Localiza o primeiro registro em um dynaset ou objeto de tipo instantâneo do <strong>Conjunto de registros</strong>, que atende aos critérios específicos e torna esse registro atual (somente para espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-132">Localiza o último registro em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (Apenas Espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p103">Localiza o próximo registro em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ). .</span><span class="sxs-lookup"><span data-stu-id="85d10-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p104">Localiza o registro anterior em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ).</span><span class="sxs-lookup"><span data-stu-id="85d10-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-140">Recupera várias linhas de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-142">Move a posição do registro atual em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-143"><strong><a href="recordset2-movefirst-method-dao.md">Métodos MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-144">Move para o primeiro registro em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="85d10-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-146">Move o último registro em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="85d10-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-148">Move o próximo registro em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="85d10-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-150">Move o registro anterior em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="85d10-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-152"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-152"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-153">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-154">Obtém o próximo conjunto de registros, quando existir, retornado por uma consulta seleção de várias partes em uma chamada <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> e retorna um valor <strong>Boolean</strong>, que indica se um ou mais registros adicionais estão pendentes (somente espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="85d10-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-156">Cria e anexa um novo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> à coleção <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-158">Atualiza os dados em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> executando novamente a consulta na qual o objeto se baseia.</span><span class="sxs-lookup"><span data-stu-id="85d10-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-160">Localiza o registro em um objeto <strong>Recordset</strong> do tipo tabela indexada que satisfaz os critérios especificados para o índice atual e torna esse registro o registro atual (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-162"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-162"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-163">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-164">Salva o conteúdo do buffer de cópia em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável.</span><span class="sxs-lookup"><span data-stu-id="85d10-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="85d10-165">Propriedades</span><span class="sxs-lookup"><span data-stu-id="85d10-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85d10-166">Nome</span><span class="sxs-lookup"><span data-stu-id="85d10-166">Name</span></span></p></th>
<th><p><span data-ttu-id="85d10-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="85d10-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85d10-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-169">Define ou retorna o número de registros relativos de um registro atual do objeto <strong>Recordset2</strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-169">Sets or returns the relative record number of a <strong>Recordset2</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-171"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-171"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-172">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-173">Retorna o número de registros que não concluíram a última atualização em lote (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="85d10-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-175"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-176">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-177">Retorna uma matriz de indicadores apontando as linhas que geraram colisões na última operação de atualização em lote (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="85d10-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-179"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-179"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-180">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-181">Define ou retorna o número de instruções enviadas de volta para o servidor em cada lote (apenas espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="85d10-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p110">Retorna um valor que indica se a posição do registro atual é antes do primeiro registro em um objeto <strong>Recordset</strong>. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p110">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-186">Define ou retorna um marcador que identifica exclusivamente o registro atual em um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-188">Retorna um valor que indica se um objeto <strong>Recordset</strong> oferece suporte a indicadores, que você pode definir utilizando a propriedade <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p111">Define ou retorna o número de registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente. <strong>Long</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="85d10-p111">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-193">Define ou retorna um valor que especifica o indicador do primeiro registro em um objeto Recordset tipo dynaset contendo dados para serem armazenados em cache localmente a partir da fonte de dados ODBC (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-195">Retorna o objeto <strong><a href="connection-object-dao.md">Connection</a></strong> que corresponde ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="85d10-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p112">Retorna a data e a hora na qual a tabela base foi criada (somente nos espaços de trabalho do Microsoft Access). <strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p112">Returns the date and time a base table was created (Microsoft Access workspaces only). Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-200">Retorna um valor que indica o estado da edição para o registro atual.</span><span class="sxs-lookup"><span data-stu-id="85d10-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p113">Retorna um valor que indica se a posição atual do registro é após o último registro em um objeto <strong>Recordset</strong>. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p113">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p114">Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p114">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-207"><strong><a href="recordset2-filter-property-dao.md">Filtro</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p115">Define ou retornar um valor que determina os registros incluídos em um objeto <strong>Recordset</strong> aberto subsequentemente (somente espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="85d10-p115">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-210"><strong><a href="recordset2-index-property-dao.md">Índice</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-211">Define ou retorna um valor que indica o nome do objeto <strong><a href="index-object-dao.md">Index</a></strong> atual em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> do tipo tabela (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-213">Retorna um bookmark que indica o registro adicionado ou alterado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="85d10-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p116">Retorna a data e a hora da alteração mais recente feita em uma tabela base. <strong>Variant</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p116">Returns the date and time of the most recent change made to a base table. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-218">Define ou retorna um valor que indica o tipo de bloqueio ativo durante a edição.</span><span class="sxs-lookup"><span data-stu-id="85d10-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p117">Retorna o nome do objeto especificado. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p117">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-223">Indica se um registro específico foi encontrado usando o método <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> ou um dos métodos <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-223">Indicates whether a particular record was found by using the <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p118">Retorna o <strong>Recordset</strong> pai do conjunto de registros especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p118">Returns the parent <strong>Recordset</strong> of the specified recordset. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-228">Define ou retorna um valor que indica o local aproximado do registro atual no objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> com base em uma porcentagem de registros no <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-228">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-229"><strong><a href="recordset2-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-229"><strong><a href="recordset2-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p119">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p119">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p120">Retorna o número de registros acessados em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> ou o número total de registros em um objeto <strong>Recordset</strong> do tipo tabela ou em um objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. <strong>Long</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p120">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-237"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-237"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-238">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-238">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-p122">Retorna um valor que indica o status de atualização do registro atual se este fizer parte de uma atualização em lotes (somente em espaços de trabalho do ODBCDirect). <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p122">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-242">Retorna um valor que indica se um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> oferece suporte ao método <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong>, que reexecuta a consulta na qual está baseado o objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="85d10-242">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-244">Define ou retorna a ordem de classificação para registros em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="85d10-244">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-246"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-246"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-247">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-247">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-248">Indica se uma operação assíncrona ou não (ou seja, um método chamado com a opção <strong>dbRunAsync</strong>) concluiu a execução (somente em espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="85d10-248">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p124">Retorna um valor que indica se um objeto aceita transactions. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p124">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-252"><strong><a href="recordset2-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-252"><strong><a href="recordset2-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p125">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>Integer</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p125">Sets or returns a value that indicates the operational type or data type of an object. Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p126">Retorna um valor que indica se você pode alterar um objeto DAO. <strong>Boolean</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p126">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-259"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="85d10-259"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="85d10-260">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="85d10-260">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="85d10-p128">Define ou retorna um valor que indica como a cláusula WHERE será construída para cada registro durante uma atualização em lotes e se a atualização em lotes deverá usar uma instrução UPDATE ou DELETE seguida de INSERT (somente em espaços de trabalho ODBCDirect). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="85d10-p128">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d10-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-264">Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="85d10-264">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d10-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="85d10-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="85d10-p129">Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto <strong>Field</strong> não satisfaça a regra de validação especificada pela definição da propriedade <strong>ValidationRule</strong> (somente nos espaços de trabalho do Microsoft Access). <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="85d10-p129">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

