---
title: Membros Field2 (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf3deac487f1e114bea2a69d5423a210a51a5944
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292794"
---
# <a name="field2-members-dao"></a>Membros Field2 (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Um objeto Field2 representa uma coluna de dados com um tipo de dados comum e um conjunto comum de propriedades.

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
<td><p><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Acrescenta dados de uma expressão de cadeia de caracteres em um objeto <strong>Field2</strong> Memo ou Long Binary em um <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Retorna todo ou parte do conteúdo de um <strong>objeto Memo</strong> ou <strong>Long BinaryField2</strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um <strong><a href="recordset-object-dao.md">objeto Recordset</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>Carrega o arquivo especificado do disco.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></p></td>
<td><p>Salva um anexo no disco.</p></td>
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
<td><p><strong><a href="field2-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se uma cadeia de caracteres de comprimento zero ( ) é uma configuração válida para a propriedade Value do objeto Field2 com um tipo de dados Texto ou Memorando (apenas espaços de trabalho do &quot; &quot; Microsoft Access). <strong><a href="field-value-property-dao.md"></a></strong> <strong></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>Obtém ou define um <strong>Boolean</strong> que indica se o campo especificado está configurado para acrescentar novos valores ao conteúdo existente do campo à medida que forem adicionados. Leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Atributos</a></strong></p></td>
<td><p>Define ou retorna um valor que indica uma ou mais características de um objeto <strong>Field2</strong>. <strong>Long</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). <strong>Long</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Retorna um objeto <strong><a href="complextype-object-dao.md">ComplexType</a></strong> que representa um campo de vários valores. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Retorna um valor que indica se os dados no campo representados por um objeto <strong>Field2</strong> são atualizáveis.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Define ou retorna o valor padrão de um objeto <strong>Field2</strong>. Para um objeto <strong>Field2</strong> ainda não acrescentado à coleção <strong><a href="fields-collection-dao.md">Fields</a></strong>, essa propriedade é de leitura/gravação (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Expression</a></strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Retorna o número de bytes usados no banco de dados (em vez de na memória) de um objeto <strong>Field2</strong> Memo ou Long Binary na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o nome do objeto <strong>Field2</strong> em uma tabela externa que corresponde a um campo em uma tabela principal de uma relação (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>Retorna um <strong>Boolean</strong> que indica se o campo especificado tem um tipo de dados de vários valores. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Define ou retorna a posição relativa de um objeto <strong>Field2</strong> em uma coleção <strong><a href="fields-collection-dao.md">Fields</a></strong>. .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Um dos <strong><a href="workspacetypeenum-enumeration-dao.md">valores de WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</p>
<p>Retorna o valor de um <strong>Field2</strong> no banco de dados que existiu quando a última atualização em lote começou (apenas espaços de trabalho ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Obrigatório</a></strong></p></td>
<td><p>Define ou retorna um valor que indica se o objeto <strong>Field2</strong> requer ou não um valor não-Nulo .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Tamanho</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o tamanho máximo, em bytes, de um objeto <strong>Field2</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Retorna um valor que indique o nome do campo que é a origem dos dados para um objeto <strong>Field2</strong>. <strong>String</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Retorna um valor que indique o nome da tabela que é a origem dos dados para um objeto <strong>Field2</strong>. <strong>String</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>número inteiro</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o valor de um objeto <strong>Field2</strong> é ou não imediatamente validado quando a propriedade <strong>Value</strong> do objeto é definida (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Define ou retorna um valor que valida os dados em um campo, conforme ele é alterado ou adicionado a uma tabela (apenas espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o texto da mensagem que o aplicativo exibe se o valor de um objeto <strong>Field2</strong> não atende à regra de validação especificada pela configuração da propriedade <strong>ValidationRule</strong> (apenas espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Valor</a></strong></p></td>
<td><p>Define ou retorna o valor de um objeto. <strong>Variant</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Um dos <strong><a href="workspacetypeenum-enumeration-dao.md">valores de WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</p>
<p>Retorna um valor atualmente no banco de dados mais recente que a propriedade <strong>OriginalValue</strong> como determinado pelo conflito de atualização em lotes (somente nos espaços de trabalho do ODBCDirect).</p></td>
</tr>
</tbody>
</table>

