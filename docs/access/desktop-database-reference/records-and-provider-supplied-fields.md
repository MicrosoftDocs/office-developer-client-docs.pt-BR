---
title: Campos fornecidos pelo provedor e registros
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ebbfeb303bb575928f09858db5d3a34cf2171ce0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300753"
---
# <a name="records-and-provider-supplied-fields"></a>Campos fornecidos pelo provedor e registros

**Aplica-se ao:** Access 2013, Office 2013

Quando um objeto [Record](record-object-ado.md) é aberto, sua origem pode ser a linha atual de um [Recordset](recordset-object-ado.md) aberto, uma URL absoluta ou uma URL relativa em conjunto com um objeto [Connection](connection-object-ado.md) aberto.

Se **Record** for aberto a partir de um **Recordset**, a coleção **Fields** com o objeto [Record](fields-collection-ado.md) conterá todos os campos do **Recordset**, além de qualquer campo adicionado pelo provedor subjacente.

O provedor pode inserir campos adicionais que funcionem como características complementares de **Record**. Como resultado, um **Record** poderá ter campos exclusivos que não façam parte de **Recordset** como um todo ou qualquer **Record** derivado de outra linha de **Recordset**.

Por exemplo, todas as linhas de um **Recordset** derivadas de uma fonte de dados de email podem ter colunas como from, to e Subject. Um **Record** derivado desse **Recordset** terá os mesmos campos. Entretanto, o **Record** também pode ter outros campos exclusivos da mensagem específica representada por esse **Record**, como Anexo e Com cópia.

Embora o objeto **Record** e a linha atual de **Recordset** tenham os mesmos campos, eles são diferentes, pois os objetos **Record** e **Recordset** possuem métodos e propriedades diferentes.

Um mesmo campo mantido por **Record** e por **Recordset** pode ser modificado em um desses dois objetos. Entretanto, ele não pode ser excluído do objeto **Record**, embora o provedor subjacente possa permitir a configuração do campo como nulo.

Depois que **Record** for aberto, você poderá adicionar campos por programação. Você também poderá excluir os campos adicionados, mas não poderá excluir campos do **Recordset** original.

Também será permitido abrir o objeto **Record** diretamente de uma URL. Nesse caso, os campos adicionados a **Record** dependerão do provedor subjacente. No momento, a maioria dos provedores adiciona um conjunto de campos que descrevem a entidade representada por **Record**. Se a entidade consistir em um fluxo de bytes, como no caso de um arquivo simples, um objeto [Stream](stream-object-ado.md) geralmente poderá ser aberto a partir de **Record**.

## <a name="special-fields-for-document-source-providers"></a>Campos especiais para provedores de fonte de documentos

Uma classe especial de provedores, denominada *provedores de fonte de documentos*, gerencia pastas e documentos. Quando um objeto **Record** representa um documento ou um objeto **Recordset** representa uma pasta de documentos, o provedor de fonte de documentos preenche esses objetos com um conjunto exclusivo de campos que descrevem as características do documento, em vez do documento real. Em geral, um campo contém uma referência a **Stream** que representa o documento.

Esses campos constituem um **record** ou um **recordset** de recurso e estão listados no [Apêndice A: Provedores](appendix-a-providers.md) para os provedores específicos que oferecem suporte a eles.

Duas constantes indexam a coleção **Fields** de um **Record** ou **Recordset** de recurso para a recuperação de um par de campos comumente utilizados. A propriedade **Value** do objeto [Field](value-property-ado.md) retorna o conteúdo desejado.

  - O campo acessado com a constante **adDefaultStream** contém um fluxo padrão associado ao objeto **Record** ou **Recordset**. O provedor atribui um fluxo padrão a um objeto.

  - O campo acessado com a constante **adRecordURL** contém a URL absoluta que identifica o documento.

Um provedor de fonte de documentos não oferece suporte à coleção [Properties](properties-collection-ado.md) dos objetos **Record** e **Field**. O conteúdo da coleção **Properties** é nulo para esses objetos.

Um provedor de fonte de documentos pode adicionar uma propriedade específica de provedor, como **Datasource Type**, para identificar um provedor desse tipo. Para obter mais informações sobre como determinar o seu tipo de provedor, consulte a documentação do provedor.

## <a name="resource-recordset-columns"></a>Colunas do conjunto de registros de recurso

Um *conjunto de registros de recurso* consiste nas seguintes colunas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da coluna</p></th>
<th><p>Tipo</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RESOURCE_PARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Somente leitura. Indica a URL do recurso.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_PARENTNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Somente leitura. Indica a URL absoluta do registro pai.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ABSOLUTEPARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Somente leitura. Indica a URL absoluta do recurso, que é a concatenação de PARENTNAME e PARSENAME.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISHIDDEN</p></td>
<td><p>AdBoolean</p></td>
<td><p>True se o recurso estiver oculto. Nenhuma linha será retornada, a menos que o comando que estiver criando o conjunto de linhas selecione explicitamente as linhas em que RESOURCE_ISHIDDEN seja True.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISREADONLY</p></td>
<td><p>AdBoolean</p></td>
<td><p>True se o recurso for somente leitura. Qualquer tentativa de abrir esse recurso com DBBINDFLAG_WRITE não terá êxito com DB_E_READONLY. Esta propriedade poderá ser editada mesmo quando o recurso for aberto somente para leitura.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTTYPE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indica o provável uso do documento —  por exemplo, o depoimento de um advogado. Isso pode corresponder ao modelo do Office usado para criar o documento.&quot;&quot;</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CONTENTCLASS</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indica o tipo MIME do documento, indicando o formato como &quot;text/html.&quot;</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTLANGUAGE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indica a linguagem na qual é armazenado o conteúdo.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CREATIONTIME</p></td>
<td><p>adFileTime</p></td>
<td><p>Somente leitura. Indica uma estrutura FILETIME contendo a hora de criação do recurso, exibida no formato da hora universal coordenada (UTC).</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_LASTACCESSTIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>Somente leitura. Indica uma estrutura FILETIME contendo a hora, em formato UTC, do último acesso ao recurso. Os membros de FILETIME terão o valor zero se o provedor não oferecer suporte a esse membro de hora.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_LASTWRITETIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>Somente leitura. Indica uma estrutura FILETIME contendo a hora, em formato UTC, da última gravação do recurso. Os membros de FILETIME terão o valor zero se o provedor não oferecer suporte a esse membro de hora.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_STREAMSIZE</p></td>
<td><p>asUnsignedBigInt</p></td>
<td><p>Somente leitura. Indica o tamanho, em bytes, do fluxo padrão do recurso.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISCOLLECTION</p></td>
<td><p>AdBoolean</p></td>
<td><p>Somente leitura. True se o recurso for uma coleção, por exemplo, um diretório. False se o recurso for um arquivo simples.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISSTRUCTUREDDOCUMENT</p></td>
<td><p>AdBoolean</p></td>
<td><p>True se o recurso for um documento estruturado. Caso contrário, será False. Pode ser uma coleção ou um arquivo simples.</p></td>
</tr>
<tr class="odd">
<td><p>DEFAULT_DOCUMENT</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Somente leitura. Indica que o recurso contém uma URL para o documento simples padrão de uma pasta ou para um documento estruturado. Usado quando o fluxo padrão for solicitado de um recurso. Esta propriedade estará em branco para um arquivo simples.</p></td>
</tr>
<tr class="even">
<td><p>CHAPTERED_CHILDREN</p></td>
<td><p>AdChapter</p></td>
<td><p>Somente leitura. Opcional. Indica o capítulo do conjunto de linhas contendo o filho do recurso. (O <em>OLE DB Provider for Internet Publishing</em> não usa esta coluna.)</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_DISPLAYNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Somente leitura. Indica o nome para exibição do recurso.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISROOT</p></td>
<td><p>AdBoolean</p></td>
<td><p>Somente leitura. True se o recurso for a raiz de uma coleção ou de um documento estruturado.</p></td>
</tr>
</tbody>
</table>

