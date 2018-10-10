---
title: Métodos do ActiveX Data Objects (ADO)
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b7a685352063c3c1dd4c9bbd62e9c1fc4cdfe11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462209"
---
# <a name="ado-methods"></a>Métodos do ADO


**Aplica-se a**: Access 2013 | Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Cria um novo registro para um objeto <strong>Recordset</strong> atualizável.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>Acrescenta um objeto a uma coleção. Se a coleção for <strong>Fields</strong>, um novo objeto <strong>Field</strong> poderá ser criado antes de ser acrescentado à coleção.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Acrescenta dados a um objeto <strong>Field</strong> ou <strong>Parameter</strong> de dados binários ou de texto longos.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans e RollbackTrans</a></p></td>
<td><p>Gerencia o processamento das transações em um objeto de <strong>Conexão</strong> da seguinte maneira: <strong>BeginTrans</strong> — inicia uma nova transação.<br />
<strong>CommitTrans</strong>  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.<br />
<strong>RollbackTrans</strong> — cancela quaisquer alterações e encerra a transação atual. Também pode iniciar uma nova transação.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Cancela a execução de uma chamada de método assíncrona pendente.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Cancela uma atualização em lotes pendente.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Cancela qualquer alteração feita na linha atual ou na nova linha de um objeto <strong>Recordset</strong>, ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, antes da chamada do método <strong>Update</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Limpar</a></p></td>
<td><p>Remove todos os objetos <strong>Error</strong> da coleção <strong>Errors</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Cria um objeto <strong>Recordset</strong> duplicado a partir de um objeto <strong>Recordset</strong> existente. Opcionalmente, especifica que o clone seja somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Fecha um objeto aberto e quaisquer objetos dependentes.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Compara dois indicadores e retorna uma indicação de seus valores relativos.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Copia um arquivo ou um diretório, e seu conteúdo, para outro local.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copia o número especificado de caracteres ou bytes (dependendo de <strong>Type</strong>) no <strong>Stream</strong> para outro objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Cria um novo objeto <strong>Parameter</strong> com as propriedades especificadas.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (coleção Parameters do ADO)</a></p></td>
<td><p>Exclui um objeto da coleção <strong>Parameters</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Excluir (coleção Fields do ADO)</a></p></td>
<td><p>Exclui um objeto da coleção <strong>Fields</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (Recordset do ADO)</a></p></td>
<td><p>Exclui o registro atual ou um grupo de registros.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">ExcluirRegistro</a></p></td>
<td><p>Exclui um arquivo ou um diretório e todos os respectivos subdiretórios.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (comando ADO)</a></p></td>
<td><p>Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (Conexão ADO)</a></p></td>
<td><p>Executes the specified query, SQL statement, stored procedure, or provider-specific text.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Localizar</a></p></td>
<td><p>Procura um <strong>Recordset</strong> para a linha que satisfaz os critérios especificados.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Liberar</a></p></td>
<td><p>Força que o com que o conteúdo do <strong>Stream</strong> remanescente no buffer do ADO vá para o objeto base com o qual o <strong>Stream</strong> está associado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Retorna um <strong>Recordset</strong> cujas linhas representam os arquivos e os subdiretórios no diretório representado por este <strong>registro</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Retorna todo, ou uma parte deles, o conteúdo do objeto <strong>Field</strong> de dados binários ou de texto longos.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Recupera vários registros de um objeto <strong>Recordset</strong> para dentro de uma matriz.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Retorna o <strong>Recordset</strong> como uma sequência.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Carrega o conteúdo de um arquivo existente para dentro de um <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Mover</a></p></td>
<td><p>Move a posição do registro atual em um objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst, MoveLast, MoveNext e MovePrevious</a></p></td>
<td><p>Move para o primeiro, o último, o próximo ou o registro anterior em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Move um arquivo, ou um diretório e seu conteúdo, para outro local.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Limpa o objeto <strong>Recordset</strong> atual e retorna o próximo <strong>Recordset</strong> avançando por uma série de comandos.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Abrir (Conexão ADO)</a></p></td>
<td><p>Abre uma conexão a uma fonte de dados.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (Record do ADO)</a></p></td>
<td><p>Abre um objeto <strong>Record</strong> existente ou cria um novo arquivo ou diretório.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open (Recordset do ADO)</a></p></td>
<td><p>Abre um cursor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open (Stream do ADO)</a></p></td>
<td><p>Abre um objeto <strong>Stream</strong> para manipular fluxos de dados de texto ou binários.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Obtém informações do esquema do banco de dados a partir do provedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Lê um número de bytes especificado a partir de um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lê um número de caracteres especificado a partir de um objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>Atualiza os objetos de uma coleção para refletir os objetos disponíveis no provedor e específicos a ele.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Atualiza os dados em um objeto <strong>Recordset</strong>, reexecutando a consulta que serve de base ao objeto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Atualiza os dados no objeto <strong>Recordset</strong> atual, ou a coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, a partir do banco de dados subjacente.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Salva o <strong>Recordset</strong> em um arquivo ou objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Salva o conteúdo binário de um <strong>Stream</strong> para um arquivo.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Pesquisa o índice de um <strong>Recordset</strong> para localizar rapidamente a linha que corresponde aos valores especificados e altera a posição de linha atual para essa linha.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Define a posição que é o final do fluxo.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Ignora uma linha inteira ao ler um fluxo de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">STAT</a></p></td>
<td><p>Obtém informações estatísticas sobre um fluxo aberto.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Suporta</a></p></td>
<td><p>Determina se um objeto <strong>Recordset</strong> especificado suporta um tipo de funcionalidade específico.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Salva quaisquer alterações feitas na linha atual de um objeto <strong>Recordset</strong> ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Grava todas as atualizações em lote pendentes no disco.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Gravação</a></p></td>
<td><p>Grava dados binários em um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Grava uma sequência de texto especificada em um objeto <strong>Stream</strong>.</p></td>
</tr>
</tbody>
</table>

