---
title: Microsoft OLE DB Provider for Microsoft Indexing Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10af40231fc10e222f818896b3d65f44ac3d6d71
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463218"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a>Microsoft OLE DB Provider for Microsoft Indexing Service


**Aplica-se a**: Access 2013 | Office 2013

O Microsoft OLE DB Provider for Microsoft Indexing Service fornece acesso programático somente leitura ao sistema de arquivos e aos dados da Web indexados pelo Serviço de Indexação da Microsoft. Os aplicativos do ADO podem emitir consultas SQL para recuperar informações sobre o conteúdo e as propriedades de arquivos.

O provedor é de encadeamento livre e habilitado para unicode.

## <a name="connection-string-parameters"></a>Parâmetros da sequência de conexão

Para estabelecer uma conexão com esse provedor, defina o argumento **Provider=** para a propriedade [ConnectionString](connectionstring-property-ado.md) como:

```vb 
 
MSIDXS 
```

A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.

## <a name="typical-connection-string"></a>Sequência de conexão típica

Esta é uma sequência de conexão típica para esse provedor:

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

A cadeia de caracteres consiste nas seguintes palavras-chave:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palavra-chave</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica o Microsoft OLE DB Provider for Microsoft Indexing Service. Geralmente, é a única palavra-chave especificada na sequência de conexão.</p></td>
</tr>
<tr class="even">
<td><p><strong>Fonte de dados</strong></p></td>
<td><p>Especifica o nome de catálogo do Serviço de Indexação. Se esta palavra-chave não for especificada, será utilizado o catálogo padrão do sistema.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Identificador de localidade </strong></p></td>
<td><p>Especifica um número único de 32 bits (por exemplo, 1033) que especifica as preferências relacionadas ao idioma do usuário. Essas preferências indicam como as datas e horários serão formatados, se os itens serão classificados em ordem alfabética, como as cadeias de caracteres serão comparadas, e assim por diante. Se esta palavra-chave não for especificada, será utilizado o identificador de localidade padrão do sistema.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Texto de comando

A sintaxe de consultas SQL do Serviço de Indexação consiste em extensões à instrução **SELECT** do SQL-92 e suas cláusulas **FROM** e **WHERE**. Os resultados da consulta são retornados pelos conjuntos de linhas do OLE DB, que podem ser consumidos pelo ADO e manipulados como objetos [Recordset](recordset-object-ado.md).

Você pode pesquisar palavras ou frases exatas ou usar curingas para pesquisar padrões ou raízes de palavras. A lógica de pesquisa pode ser baseada em decisões booleanas, em termos balanceados ou na proximidade de outras palavras. Também é possível realizar pesquisas baseadas em "texto livre", que localizam coincidências com base no significado e não em palavras exatas.

O provedor não aceita chamadas de procedimento armazenado ou nomes simples de tabelas (por exemplo, a propriedade [CommandType](commandtype-property-ado.md) sempre será **adCmdText**).

## <a name="recordset-behavior"></a>Comportamento do Recordset

As tabelas a seguir listam os recursos disponíveis em um objeto **Recordset** aberto com esse provedor. Somente o tipo de cursor estático (**adOpenStatic**) está disponível.

Para obter informações mais detalhadas sobre o comportamento do **Recordset** na sua configuração de provedor, execute o método [Supports](supports-method-ado.md) e enumere a coleção [Properties](properties-collection-ado.md) de **Recordset** para identificar se propriedades dinâmicas específicas para provedor estão presentes.

Disponibilidade das propriedades padrão do **Recordset** do ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propriedade</p></th>
<th><p>Disponibilidade</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Indicador</a>*</p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>sempre <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>sempre <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>sempre <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>não disponível</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Origem</a></p></td>
<td><p>leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">Estado</a></p></td>
<td><p>somente leitura</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>somente leitura</p></td>
</tr>
</tbody>
</table>


\*Indicadores devem estar habilitados no provedor para que este recurso exista no **Recordset**.

Disponibilidade dos métodos padrão do **Recordset** do ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método</p></th>
<th><p>Disponível?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Mover</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="supports-method-ado.md">Suporta</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Não</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

Para obter detalhes específicos de implementação e informações funcionais sobre o Microsoft OLE DB Provider for Microsoft Indexing Service, consulte de referência o Microsoft OLE DB do programador.

