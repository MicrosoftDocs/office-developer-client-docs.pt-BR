---
title: Métodos de ActiveX Data Objects (ADO)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d5b08478b714a9b70e5cb08daff6e04b8883071
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026376"
---
# <a name="ado-methods"></a><span data-ttu-id="aabd6-102">Métodos do ADO</span><span class="sxs-lookup"><span data-stu-id="aabd6-102">ADO methods</span></span>

<span data-ttu-id="aabd6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="aabd6-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="aabd6-104">Método</span><span class="sxs-lookup"><span data-stu-id="aabd6-104">Method</span></span></th>
<th><span data-ttu-id="aabd6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="aabd6-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-107">Cria um novo registro para um objeto <strong>Recordset</strong> atualizável.</span><span class="sxs-lookup"><span data-stu-id="aabd6-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-108"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-p101">Acrescenta um objeto a uma coleção. Se a coleção for <strong>Fields</strong>, um novo objeto <strong>Field</strong> poderá ser criado antes de ser acrescentado à coleção.</span><span class="sxs-lookup"><span data-stu-id="aabd6-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-112">Acrescenta dados a um objeto <strong>Field</strong> ou <strong>Parameter</strong> de dados binários ou de texto longos.</span><span class="sxs-lookup"><span data-stu-id="aabd6-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans e RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-114">Gerencia o processamento de transações em um objeto <strong>Connection</strong> da seguinte maneira:
</span><span class="sxs-lookup"><span data-stu-id="aabd6-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="aabd6-115"><strong>BeginTrans</strong>  inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="aabd6-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="aabd6-p102">
<strong>CommitTrans</strong>  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="aabd6-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="aabd6-118">
<strong>RollbackTrans</strong> — cancela quaisquer alterações e encerra a transação atual.</span><span class="sxs-lookup"><span data-stu-id="aabd6-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="aabd6-119">Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="aabd6-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-120"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-121">Cancela a execução de uma chamada de método assíncrona pendente.</span><span class="sxs-lookup"><span data-stu-id="aabd6-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-123">Cancela uma atualização em lotes pendente.</span><span class="sxs-lookup"><span data-stu-id="aabd6-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-125">Cancela qualquer alteração feita na linha atual ou na nova linha de um objeto <strong>Recordset</strong>, ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, antes da chamada do método <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-127">Remove todos os objetos <strong>Error</strong> da coleção <strong>Errors</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-p104">Cria um objeto <strong>Recordset</strong> duplicado a partir de um objeto <strong>Recordset</strong> existente. Opcionalmente, especifica que o clone seja somente leitura.</span><span class="sxs-lookup"><span data-stu-id="aabd6-p104">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object. Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-132">Fecha um objeto aberto e quaisquer objetos dependentes.</span><span class="sxs-lookup"><span data-stu-id="aabd6-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-134">Compara dois indicadores e retorna uma indicação de seus valores relativos.</span><span class="sxs-lookup"><span data-stu-id="aabd6-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-136">Copia um arquivo ou um diretório, e seu conteúdo, para outro local.</span><span class="sxs-lookup"><span data-stu-id="aabd6-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-138">Copia o número especificado de caracteres ou bytes (dependendo de <strong>Type</strong>) no <strong>Stream</strong> para outro objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-140">Cria um novo objeto <strong>Parameter</strong> com as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="aabd6-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-141"><a href="delete-method-ado-parameters-collection.md">Delete (coleção Parameters do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-142">Exclui um objeto da coleção <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-143"><a href="delete-method-ado-fields-collection.md">Excluir (coleção Fields do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-144">Exclui um objeto da coleção <strong>Fields</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-145"><a href="delete-method-ado-recordset.md">Delete (Recordset do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-146">Exclui o registro atual ou um grupo de registros.</span><span class="sxs-lookup"><span data-stu-id="aabd6-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-147"><a href="deleterecord-method-ado.md">ExcluirRegistro</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-148">Exclui um arquivo ou um diretório e todos os respectivos subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="aabd6-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (comando ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span><span class="sxs-lookup"><span data-stu-id="aabd6-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (Conexão ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span><span class="sxs-lookup"><span data-stu-id="aabd6-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-153"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-154">Procura um <strong>Recordset</strong> para a linha que satisfaz os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="aabd6-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-155"><a href="flush-method-ado.md">Liberar</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-156">Força que o com que o conteúdo do <strong>Stream</strong> remanescente no buffer do ADO vá para o objeto base com o qual o <strong>Stream</strong> está associado.</span><span class="sxs-lookup"><span data-stu-id="aabd6-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-158">Retorna um <strong>Recordset</strong> cujas linhas representam os arquivos e os subdiretórios no diretório representado por este <strong>registro</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-160">Retorna todo, ou uma parte deles, o conteúdo do objeto <strong>Field</strong> de dados binários ou de texto longos.</span><span class="sxs-lookup"><span data-stu-id="aabd6-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-162">Recupera vários registros de um objeto <strong>Recordset</strong> para dentro de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="aabd6-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-164">Retorna o <strong>Recordset</strong> como uma sequência.</span><span class="sxs-lookup"><span data-stu-id="aabd6-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-166">Carrega o conteúdo de um arquivo existente para dentro de um <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-167"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-168">Move a posição do registro atual em um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst, MoveLast, MoveNext e MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-170">Move para o primeiro, o último, o próximo ou o registro anterior em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</span><span class="sxs-lookup"><span data-stu-id="aabd6-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-172">Move um arquivo, ou um diretório e seu conteúdo, para outro local.</span><span class="sxs-lookup"><span data-stu-id="aabd6-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-174">Limpa o objeto <strong>Recordset</strong> atual e retorna o próximo <strong>Recordset</strong> avançando por uma série de comandos.</span><span class="sxs-lookup"><span data-stu-id="aabd6-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-175"><a href="open-method-ado-connection.md">Abrir (Conexão ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-176">Abre uma conexão a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="aabd6-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-177"><a href="open-method-ado-record.md">Open (Record do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-178">Abre um objeto <strong>Record</strong> existente ou cria um novo arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="aabd6-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-179"><a href="open-method-ado-recordset.md">Open (Recordset do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-180">Abre um cursor.</span><span class="sxs-lookup"><span data-stu-id="aabd6-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-181"><a href="open-method-ado-stream.md">Open (Stream do ADO)</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-182">Abre um objeto <strong>Stream</strong> para manipular fluxos de dados de texto ou binários.</span><span class="sxs-lookup"><span data-stu-id="aabd6-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-184">Obtém informações do esquema do banco de dados a partir do provedor.</span><span class="sxs-lookup"><span data-stu-id="aabd6-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-185"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-186">Lê um número de bytes especificado a partir de um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-188">Lê um número de caracteres especificado a partir de um objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="aabd6-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-190">Atualiza os objetos de uma coleção para refletir os objetos disponíveis no provedor e específicos a ele.</span><span class="sxs-lookup"><span data-stu-id="aabd6-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-191"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-192">Atualiza os dados em um objeto <strong>Recordset</strong>, reexecutando a consulta que serve de base ao objeto.</span><span class="sxs-lookup"><span data-stu-id="aabd6-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-193"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-194">Atualiza os dados no objeto <strong>Recordset</strong> atual, ou a coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, a partir do banco de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="aabd6-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-196">Salva o <strong>Recordset</strong> em um arquivo ou objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-198">Salva o conteúdo binário de um <strong>Stream</strong> para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="aabd6-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-200">Pesquisa o índice de um <strong>Recordset</strong> para localizar rapidamente a linha que corresponde aos valores especificados e altera a posição de linha atual para essa linha.</span><span class="sxs-lookup"><span data-stu-id="aabd6-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-202">Define a posição que é o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="aabd6-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-204">Ignora uma linha inteira ao ler um fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="aabd6-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-206">Obtém informações estatísticas sobre um fluxo aberto.</span><span class="sxs-lookup"><span data-stu-id="aabd6-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-207"><a href="supports-method-ado.md">Suporta</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-208">Determina se um objeto <strong>Recordset</strong> especificado suporta um tipo de funcionalidade específico.</span><span class="sxs-lookup"><span data-stu-id="aabd6-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-209"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-210">Salva quaisquer alterações feitas na linha atual de um objeto <strong>Recordset</strong> ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-212">Grava todas as atualizações em lote pendentes no disco.</span><span class="sxs-lookup"><span data-stu-id="aabd6-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aabd6-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-214">Grava dados binários em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aabd6-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="aabd6-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="aabd6-216">Grava uma sequência de texto especificada em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="aabd6-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>