---
title: Microsoft OLE DB Provider for Microsoft Active Directory Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ad3b3163a2169d90072335d5bc827700b99c73f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462855"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a>Microsoft OLE DB Provider for Microsoft Active Directory Service

**Aplica-se a**: Access 2013 | Office 2013

O provedor ADSI (Interfaces de Serviços do Active Directory) da Microsoft permite que o ADO conecte-se a serviços de diretório heterogêneos por meio de ADSI. Isso fornece aos aplicativos do ADO acesso somente leitura aos serviços de diretório do Microsoft Windows NT 4.0 e Microsoft Windows 2000, além de qualquer serviço de diretório compatível com o LDAP e os Serviços de Diretório da Novell. O ADSI em si é baseado em um modelo de provedor, portanto, se houver um novo provedor fornecendo acesso a outro diretório, o aplicativo do ADO poderá acessá-lo sem qualquer problema. O provedor ADSI é de encadeamento livre e habilitado para unicode.

## <a name="connection-string-parameters"></a>Parâmetros de sequência de conexão

Para conectar-se a esse provedor, defina o argumento **Provider** da propriedade [ConnectionString](connectionstring-property-ado.md) como:

```vb 
 
ADSDSOObject 
```

A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.

## <a name="typical-connection-string"></a>Sequência de conexão típica

Esta é uma sequência de conexão típica para esse provedor:

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
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
<td><p>Especifica o Microsoft OLE DB Provider for Microsoft Indexing Service.</p></td>
</tr>
<tr class="even">
<td><p><strong>User ID</strong></p></td>
<td><p>Especifica o nome do usuário. Se essa palavra-chave for omitida, o logon atual será utilizado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica a senha do usuário. Se essa palavra-chave for omitida, o logon atual será utilizado.</p></td>
</tr>
</tbody>
</table>


**Texto de comando**

Uma sequência de texto de comando de quatro partes é reconhecida pelo provedor na seguinte sintaxe:

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Raiz</em></p></td>
<td><p>Indica o objeto <strong>ADsPath</strong> a partir do qual iniciar a pesquisa (isto é, a raiz para a pesquisa).</p></td>
</tr>
<tr class="even">
<td><p><em>Filter</em></p></td>
<td><p>Indica o filtro da pesquisa no formato RFC 1960.</p></td>
</tr>
<tr class="odd">
<td><p><em>Attributes</em></p></td>
<td><p>Indica uma lista de atributos a ser retornada, delimitada por vírgula.</p></td>
</tr>
<tr class="even">
<td><p><em>Scope</em></p></td>
<td><p>Opcional. Uma <strong>cadeia de caracteres</strong> que especifica o escopo da pesquisa. Pode ser uma das seguintes opções: Base — pesquisa somente o objeto base (raiz da pesquisa).<br />
OneLevel — Pesquisa somente um nível.<br />
Subárvore — Pesquisa a subárvore inteira.</p></td>
</tr>
</tbody>
</table>


Por exemplo:

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

O provedor também oferece suporte à SQL SELECT para o texto de comando. Por exemplo:

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

O provedor não aceita chamadas de procedimento armazenado ou nomes simples de tabelas (por exemplo, a propriedade [CommandType](commandtype-property-ado.md) sempre será **adCmdText**). Consulte a documentação das Interfaces de Serviços do Active Directory para obter uma descrição mais completa dos elementos do texto de comando.

## <a name="recordset-behavior"></a>Comportamento do Recordset

As tabelas a seguir relacionam os recursos disponíveis em um objeto [Recordset](recordset-object-ado.md) aberto com este provedor. Somente o tipo de cursor estático (**adOpenStatic**) está disponível.

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
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
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
<td><p>Não</p></td>
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
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Suporta</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Não</p></td>
</tr>
</tbody>
</table>
