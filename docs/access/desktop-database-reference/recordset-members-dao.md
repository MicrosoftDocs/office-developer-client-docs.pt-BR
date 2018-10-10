---
title: Membros do conjunto de registros (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2989159683b668c798181c2e99d58fade8fba467
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464398"
---
# <a name="recordset-members-dao"></a>Membros do conjunto de registros (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Um objeto Recordset representa os registros em uma tabela base ou os registros resultantes da execução de uma consulta.

## <a name="methods"></a>Métodos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></p></td>
<td><p>Cria um novo registro para um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cancel-method-dao.md">Cancelar</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Cancela a execução de uma chamada assíncrona pendente do método (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p>Cancela quaisquer atualizações pendentes para um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>Cria um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> duplicado que faz referência ao objeto <strong>Recordset</strong> original.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-close-method-dao.md">Fechar</a></strong></p></td>
<td><p>Fecha um <strong>Recordset</strong> aberto.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>Retorna um objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong> que é uma cópia do <strong>QueryDef</strong> usado para criar o objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> representado por um espaço reservado recordset (somente espaços de trabalho do Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-delete-method-dao.md">Excluir</a></strong></p></td>
<td><p>Não aceito para este objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>Copia o registro atual de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável para o buffer de cópia para edição subsequente.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Preenche parcial ou totalmente um cache local de um objeto <strong>Recordset</strong> que contém dados de uma fonte de dados ODBC conectada ao mecanismo de banco de dados do Microsoft Access (somente bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>Localiza o primeiro registro em um dynaset ou objeto de tipo instantâneo do <strong>Conjunto de registros</strong>, que atende aos critérios específicos e torna esse registro atual (somente para espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>Localiza o último registro em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (Apenas Espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>Localiza o próximo registro em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>Localiza o registro anterior em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p>Recupera várias linhas de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-move-method-dao.md">Mover</a></strong></p></td>
<td><p>Move a posição do registro atual em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movefirst-method-dao.md">Métodos MoveFirst</a></strong></p></td>
<td><p>Move para o primeiro registro em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>Move o último registro em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>Move o próximo registro em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>Move o registro anterior em um objeto <strong>Recordset</strong> especificado e torna esse registro o atual.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Obtém o próximo conjunto de registros, quando existir, retornado por uma consulta seleção de várias partes em uma chamada <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> e retorna um valor <strong>Boolean</strong>, que indica se um ou mais registros adicionais estão pendentes (somente espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Cria e anexa um novo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> à coleção <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></p></td>
<td><p>Atualiza os dados em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> executando novamente a consulta na qual o objeto se baseia.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></p></td>
<td><p>Localiza o registro em um objeto <strong>Recordset</strong> do tipo tabela indexada que satisfaz os critérios especificados para o índice atual e torna esse registro o registro atual (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-update-method-dao.md">Atualizar</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Salva o conteúdo do buffer de cópia em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> atualizável.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propriedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></p></td>
<td><p>Define ou retorna o número de registro relativo do registro atual de um objeto <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Retorna o número de registros que não concluíram a última atualização em lote (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Retorna uma matriz de indicadores apontando as linhas que geraram colisões na última operação de atualização em lote (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Define ou retorna o número de instruções enviadas de volta para o servidor em cada lote (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>Retorna um valor que indica se a posição do registro atual é antes do primeiro registro em um objeto <strong>Recordset</strong>. <strong>Boolean</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-bookmark-property-dao.md">Indicador</a></strong></p></td>
<td><p>Define ou retorna um Bookmark que identifica exclusivamente o registro atual em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p>Retorna um valor que indica se um objeto <strong>Recordset</strong> oferece suporte a indicadores, que você pode definir utilizando a propriedade <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Define ou retorna o número de registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente. <strong>Long</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o indicador do primeiro registro em um objeto Recordset tipo dynaset contendo dados para serem armazenados em cache localmente a partir da fonte de dados ODBC (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></p></td>
<td><p>Retorna o objeto <strong><a href="connection-object-dao.md">Connection</a></strong> que corresponde ao banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Retorna a data e a hora na qual a tabela base foi criada (somente nos espaços de trabalho do Microsoft Access). <strong>Variant</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>Retorna um valor que indica o estado da edição para o registro atual.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>Retorna um valor que indica se a posição atual do registro é após o último registro em um objeto <strong>Recordset</strong>. <strong>Boolean</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-filter-property-dao.md">Filtro</a></strong></p></td>
<td><p>Define ou retornar um valor que determina os registros incluídos em um objeto <strong>Recordset</strong> aberto subsequentemente (somente espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-index-property-dao.md">Índice</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o nome do objeto <strong><a href="index-object-dao.md">Index</a></strong> atual em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> do tipo tabela (somente nos espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>Retorna um bookmark que indica o registro adicionado ou alterado mais recentemente.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Retorna a data e a hora da alteração mais recente feita em uma tabela base. <strong>Variant</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o tipo de bloqueio ativo durante a edição.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-name-property-dao.md">Nome</a></strong></p></td>
<td><p>Retorna o nome do objeto especificado. <strong>String</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p>Indica se um registro específico foi encontrado usando o método <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> ou um dos métodos <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> (somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o local aproximado do registro atual no objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> com base em uma porcentagem de registros no <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-properties-property-dao.md">Propriedades</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Retorna o número de registros acessados em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> ou o número total de registros em um objeto <strong>Recordset</strong> do tipo tabela ou em um objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. <strong>Long</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Retorna um valor que indica o status de atualização do registro atual se este fizer parte de uma atualização em lotes (somente em espaços de trabalho do ODBCDirect). <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p>Retorna um valor que indica se um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> oferece suporte ao método <strong><a href="recordset-requery-method-dao.md">Requery</a></strong>, que reexecuta a consulta na qual está baseado o objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></p></td>
<td><p>Define ou retorna a ordem de classificação para registros em um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> (somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Indica se uma operação assíncrona ou não (ou seja, um método chamado com a opção <strong>dbRunAsync</strong>) concluiu a execução (somente em espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Retorna um valor que indica se um objeto aceita transactions. <strong>Boolean</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo</strong></p></td>
<td><p>A descrição deste membro aparecerá na versão final do Office 14.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Retorna um valor que indica se você pode alterar um objeto DAO. <strong>Boolean</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p>Define ou retorna um valor que indica como a cláusula WHERE será construída para cada registro durante uma atualização em lotes e se a atualização em lotes deverá usar uma instrução UPDATE ou DELETE seguida de INSERT (somente em espaços de trabalho ODBCDirect). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> de leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto <strong>Field</strong> não satisfaça a regra de validação especificada pela definição da propriedade <strong>ValidationRule</strong> (somente nos espaços de trabalho do Microsoft Access). <strong>String</strong> somente leitura.</p></td>
</tr>
</tbody>
</table>

