---
title: Membros do campo (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 497c0375496310c27c134792e01bd17e5533a452
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922199"
---
# <a name="field-members-dao"></a>Membros do campo (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Um objeto Field representa uma coluna de dados com um tipo de dados comum e um conjunto comum de propriedades.

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
<td><p><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Acrescenta dados de uma expressão de cadeia de caracteres a um objeto <strong><a href="field-object-dao.md">Field</a></strong> Memo ou Long Binary em um <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Retorna o conteúdo no todo ou em parte de um objeto <strong><strong>Field</strong></strong> <a href="field-object-dao.md">Memo</a> ou <strong>Long Binary</strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
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
<td><p><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se uma cadeia de caracteres de comprimento zero (&quot;&quot;) é uma configuração válida para a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> do objeto <strong><a href="field-object-dao.md">Field</a></strong> com um tipo de dados texto ou memorando (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-attributes-property-dao.md">Atributos</a></strong></p></td>
<td><p>Define ou retorna um valor que indica uma ou mais características de um objeto <strong><a href="field-object-dao.md">Field</a></strong>. <strong>Long</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). <strong>Long</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Retorna um valor que indica se os dados no campo representados por um objeto <strong><a href="field-object-dao.md">Field</a></strong> são atualizáveis.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Define ou retorna o valor padrão de um objeto <strong><a href="field-object-dao.md">Field</a></strong>. Para um objeto <strong>Field</strong> ainda não acrescentado à coleção <strong><a href="fields-collection-dao.md">Fields</a></strong>, essa propriedade é de leitura/gravação (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-fieldsize-property-dao.md">Tamanho do campo</a></strong></p></td>
<td><p>Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary <strong><a href="field-object-dao.md">Field</a></strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o nome do objeto <strong><a href="field-object-dao.md">Field</a></strong> em uma tabela externa que corresponde a um campo em uma tabela primária de uma relação (somente nos espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-name-property-dao.md">Nome</a></strong></p></td>
<td><p>Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Define ou retorna a posição relativa de um objeto <strong><a href="field-object-dao.md">Field</a></strong> em uma coleção <strong><a href="fields-collection-dao.md">Fields</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.


<p>Retorna o valor de um <strong>Field</strong> no banco de dados existente quando começou a última atualização em lotes (somente nos espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Propriedades</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">Necessário</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se um objeto <strong><a href="field-object-dao.md">Field</a></strong> requer um valor não Null.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">Tamanho</a></strong></p></td>
<td><p>Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary <strong><a href="field-object-dao.md">Field</a></strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Retorna um valor que indica o nome do campo que é a fonte de dados original de um objeto <strong>Field</strong>. <strong>String</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Retorna um valor que indica o nome da tabela que é a fonte de dados original de um objeto <strong>Field</strong>. <strong>String</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>Integer</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica ou não se o valor de um objeto <strong><a href="field-object-dao.md">Field</a></strong> será imediatamente validado quando a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> do objeto será definida (somente em espaços de trabalho Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto <strong>Field</strong> não satisfaça a regra de validação especificada pela definição da propriedade <strong>ValidationRule</strong> (somente nos espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-value-property-dao.md">Valor</a></strong></p></td>
<td><p>Define ou retorna o valor de um objeto. <strong>Variant</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.


<p>Retorna um valor atualmente no banco de dados mais recente que a propriedade <strong>OriginalValue</strong> como determinado pelo conflito de atualização em lotes (somente nos espaços de trabalho do ODBCDirect).</p></td>
</tr>
</tbody>
</table>

