---
title: Métodos do ActiveX Data Objects (ADO)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3169b7eaab6ad290bfc385881f5de69edc80111f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283279"
---
# <a name="ado-methods"></a><span data-ttu-id="6c2a4-102">Métodos do ADO</span><span class="sxs-lookup"><span data-stu-id="6c2a4-102">ADO methods</span></span>

<span data-ttu-id="6c2a4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c2a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="6c2a4-104">Método		</span><span class="sxs-lookup"><span data-stu-id="6c2a4-104">Method</span></span></th>
<th><span data-ttu-id="6c2a4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c2a4-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-107">Cria um novo registro para um objeto <strong>Recordset</strong> que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-108"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-p101">Acrescenta um objeto a uma coleção. Se a coleção for <strong>Fields</strong>, um novo objeto <strong>Field</strong> poderá ser criado antes de ser acrescentado à coleção.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-112">Acrescenta dados a um objeto <strong>Field</strong> com dados binários ou texto grande, ou a um objeto <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans e RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-114">Gerencia o processamento de transações em um objeto <strong>Connection</strong> da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6c2a4-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="6c2a4-115"><strong>BeginTrans</strong>  inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="6c2a4-p102">
<strong>CommitTrans</strong>  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="6c2a4-118">
<strong>RollbackTrans</strong> — cancela as alterações e encerra a transação atual.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="6c2a4-119">Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-120"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-121">Cancela a execução de uma chamada de método assíncrono, pendente.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-123">Cancela uma atualização em lote pendente.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-125">Cancela quaisquer alterações feitas em uma linha atual ou nova de um objeto <strong>Recordset</strong>, ou da coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, antes de chamar o método <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-127">Remove todos os objetos <strong>Error</strong> da coleção <strong>Errors</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-129">Cria um objeto <strong>Recordset</strong> duplicado a partir de um objeto <strong>Recordset</strong> existente.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-129">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="6c2a4-130">Opcionalmente, especifica que o clone pode ser somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-130">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-132">Fecha um objeto aberto e quaisquer objetos dependentes.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-134">Compara dois indicadores e retorna uma indicação de seus valores relativos.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-136">Copia um arquivo ou um diretório, e seu conteúdo, para outro local.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-138">Copia o número especificado de caracteres ou bytes (dependendo do <strong>Tipo</strong>) de um objeto <strong>Stream</strong> para outro <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-140">Cria um novo objeto <strong>Parameter</strong> com propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-141"><a href="delete-method-ado-parameters-collection.md">Delete (Coleção Parameters do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-142">Exclui um objeto da coleção <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-143"><a href="delete-method-ado-fields-collection.md">Delete (Coleção Fields do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-144">Exclui um objeto da coleção <strong>Fields</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-145"><a href="delete-method-ado-recordset.md">Delete (Recordset do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-146">Exclui o registro atual ou um grupo de registros.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-147"><a href="deleterecord-method-ado.md">ExcluirRegistro</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-148">Exclui um arquivo ou diretório e todos os seus subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (Command do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-150">Executa a consulta, a instrução SQL, ou o procedimento armazenado especificado na propriedade <strong>CommandText</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (Connection do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-152">Executa a consulta especificada, a instrução SQL, o procedimento armazenado ou o texto específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-153"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-154">Pesquisa um <strong>Recordset</strong> para a linha que atende aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-155"><a href="flush-method-ado.md">Descarga</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-156">Força o conteúdo do <strong>Stream</strong> a permanecer no buffer do objeto de base ao qual o <strong>Stream</strong> está associado.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-158">Retorna um <strong>Recordset</strong> cujas linhas representam os arquivos e os subdiretórios no diretório representado por este <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-160">Retorna todos os conteúdos, ou uma parte deles, de um texto amplo ou de um objeto<strong>Field</strong> de dados binários.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-162">Recupera vários registros de um objeto <strong>Recordset</strong> dentro de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-164">Retorna o <strong>Recordset</strong> como uma sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-166">Carrega os conteúdos de um arquivo existente em um <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-167"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-168">Move a posição do registro atual em um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext e MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-170">Move o registro para primeiro, último, próximo ou anterior em um objeto <strong>Recordset</strong> especificado, tornando-o atual.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-172">Move um arquivo, ou um diretório e seus contéudos, para outro local.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-174">Limpa o objeto <strong>Recordset</strong> atual e retorna o próximo <strong>Recordset</strong> avançando por uma série de comandos.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-175"><a href="open-method-ado-connection.md">Open (Connection do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-176">Abre uma conexão para uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-177"><a href="open-method-ado-record.md">Open (Record do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-178">Abre um objeto <strong>Record</strong> existente, ou cria um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-179"><a href="open-method-ado-recordset.md">Open (Recordset do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-180">Abre um cursor.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-181"><a href="open-method-ado-stream.md">Open (Stream do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-182">Abre um objeto <strong>Stream</strong> para manipular fluxos de dados binários ou de texto.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-184">Obtém informações do esquema do banco de dados a partir do provedor.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-185"><a href="read-method-ado.md">Leitura</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-186">Lê um número de bytes especificado a partir de um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-188">Lê um número de caracteres especificado a partir de um objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-190">Atualiza os objetos em uma coleção para refletir objetos disponíveis a partir do provedor e para o provedor específico.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-191"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-192">Atualiza os dados em um objeto <strong>Recordset</strong> ao executar novamente a consulta na qual se baseia o objeto.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-193"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-194">Atualiza os dados no objeto <strong>Recordset</strong> atual, ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, a partir do banco de dados de base.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-196">Salva o <strong>Recordset</strong> em um arquivo ou objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-198">Salva o conteúdo binário de um <strong>Stream</strong> em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-200">Pesquisa o índice de um <strong>Recordset</strong> para localizar rapidamente a linha que corresponde aos valores especificados e altera a posição da linha atual para essas linha.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-202">Define a posição para o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-204">Ignora uma linha inteira ao ler um fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-206">Obtém informações estatísticas sobre um fluxo aberto.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-207"><a href="supports-method-ado.md">Compatível</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-208">Determina se um objeto <strong>Recordset</strong> especificado oferece suporte a um tipo específico de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-209"><a href="update-method-ado.md">Atualização</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-210">Salva quaisquer alterações feitas na linha atual de um objeto <strong>Recordset</strong>, ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-212">Grava no disco todas as atualizações em lote pendentes.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c2a4-213"><a href="write-method-ado.md">Escrever</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-214">Grava dados binários em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2a4-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="6c2a4-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="6c2a4-216">Grava uma sequência de texto especificada em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
