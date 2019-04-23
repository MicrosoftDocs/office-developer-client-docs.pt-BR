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
# <a name="ado-methods"></a>Métodos do ADO

**Aplica-se ao:** Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Método		</th>
<th>Descrição</th>
</tr>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Cria um novo registro para um objeto <strong>Recordset</strong> que pode ser atualizado.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>Acrescenta um objeto a uma coleção. Se a coleção for <strong>Fields</strong>, um novo objeto <strong>Field</strong> poderá ser criado antes de ser acrescentado à coleção.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Acrescenta dados a um objeto <strong>Field</strong> com dados binários ou texto grande, ou a um objeto <strong>Parameter</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans e RollbackTrans</a></p></td>
<td><p>Gerencia o processamento de transações em um objeto <strong>Connection</strong> da seguinte maneira:<br/><br/><strong>BeginTrans</strong>  inicia uma nova transação.<br/><br/>
<strong>CommitTrans</strong>  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.<br/><br/>
<strong>RollbackTrans</strong> — cancela as alterações e encerra a transação atual. Também pode iniciar uma nova transação.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Cancela a execução de uma chamada de método assíncrono, pendente.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Cancela uma atualização em lote pendente.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Cancela quaisquer alterações feitas em uma linha atual ou nova de um objeto <strong>Recordset</strong>, ou da coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, antes de chamar o método <strong>Update</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p>Remove todos os objetos <strong>Error</strong> da coleção <strong>Errors</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Cria um objeto <strong>Recordset</strong> duplicado a partir de um objeto <strong>Recordset</strong> existente. Opcionalmente, especifica que o clone pode ser somente leitura.</p></td>
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
<td><p>Copia o número especificado de caracteres ou bytes (dependendo do <strong>Tipo</strong>) de um objeto <strong>Stream</strong> para outro <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Cria um novo objeto <strong>Parameter</strong> com propriedades especificadas.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (Coleção Parameters do ADO)</a></p></td>
<td><p>Exclui um objeto da coleção <strong>Parameters</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Delete (Coleção Fields do ADO)</a></p></td>
<td><p>Exclui um objeto da coleção <strong>Fields</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (Recordset do ADO)</a></p></td>
<td><p>Exclui o registro atual ou um grupo de registros.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">ExcluirRegistro</a></p></td>
<td><p>Exclui um arquivo ou diretório e todos os seus subdiretórios.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (Command do ADO)</a></p></td>
<td><p>Executa a consulta, a instrução SQL, ou o procedimento armazenado especificado na propriedade <strong>CommandText</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (Connection do ADO)</a></p></td>
<td><p>Executa a consulta especificada, a instrução SQL, o procedimento armazenado ou o texto específico do provedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p>Pesquisa um <strong>Recordset</strong> para a linha que atende aos critérios especificados.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Descarga</a></p></td>
<td><p>Força o conteúdo do <strong>Stream</strong> a permanecer no buffer do objeto de base ao qual o <strong>Stream</strong> está associado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Retorna um <strong>Recordset</strong> cujas linhas representam os arquivos e os subdiretórios no diretório representado por este <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Retorna todos os conteúdos, ou uma parte deles, de um texto amplo ou de um objeto<strong>Field</strong> de dados binários.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Recupera vários registros de um objeto <strong>Recordset</strong> dentro de uma matriz.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Retorna o <strong>Recordset</strong> como uma sequência de caracteres.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Carrega os conteúdos de um arquivo existente em um <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Move a posição do registro atual em um objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext e MovePrevious</a></p></td>
<td><p>Move o registro para primeiro, último, próximo ou anterior em um objeto <strong>Recordset</strong> especificado, tornando-o atual.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Move um arquivo, ou um diretório e seus contéudos, para outro local.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Limpa o objeto <strong>Recordset</strong> atual e retorna o próximo <strong>Recordset</strong> avançando por uma série de comandos.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (Connection do ADO)</a></p></td>
<td><p>Abre uma conexão para uma fonte de dados.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (Record do ADO)</a></p></td>
<td><p>Abre um objeto <strong>Record</strong> existente, ou cria um arquivo ou diretório.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open (Recordset do ADO)</a></p></td>
<td><p>Abre um cursor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open (Stream do ADO)</a></p></td>
<td><p>Abre um objeto <strong>Stream</strong> para manipular fluxos de dados binários ou de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Obtém informações do esquema do banco de dados a partir do provedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Leitura</a></p></td>
<td><p>Lê um número de bytes especificado a partir de um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lê um número de caracteres especificado a partir de um objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>Atualiza os objetos em uma coleção para refletir objetos disponíveis a partir do provedor e para o provedor específico.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Atualiza os dados em um objeto <strong>Recordset</strong> ao executar novamente a consulta na qual se baseia o objeto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Atualiza os dados no objeto <strong>Recordset</strong> atual, ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>, a partir do banco de dados de base.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Salva o <strong>Recordset</strong> em um arquivo ou objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Salva o conteúdo binário de um <strong>Stream</strong> em um arquivo.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Pesquisa o índice de um <strong>Recordset</strong> para localizar rapidamente a linha que corresponde aos valores especificados e altera a posição da linha atual para essas linha.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Define a posição para o final do fluxo.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Ignora uma linha inteira ao ler um fluxo de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Obtém informações estatísticas sobre um fluxo aberto.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Compatível</a></p></td>
<td><p>Determina se um objeto <strong>Recordset</strong> especificado oferece suporte a um tipo específico de funcionalidade.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Atualização</a></p></td>
<td><p>Salva quaisquer alterações feitas na linha atual de um objeto <strong>Recordset</strong>, ou na coleção <strong>Fields</strong> de um objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Grava no disco todas as atualizações em lote pendentes.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Escrever</a></p></td>
<td><p>Grava dados binários em um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Grava uma sequência de texto especificada em um objeto <strong>Stream</strong>.</p></td>
</tr>
</tbody>
</table>

<br/>
