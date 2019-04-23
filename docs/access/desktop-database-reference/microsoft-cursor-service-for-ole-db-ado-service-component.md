---
title: Microsoft Cursor Service for OLE DB (Componente de Serviço do ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d79d060922c6e7f28209242ebe82821c2ba97bfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288985"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a>Serviço de cursor da Microsoft para OLE DB (Componente de serviços ADO)


**Aplica-se ao:** Access 2013, Office 2013

O Microsoft Cursor Service for OLE DB complementa as funções de suporte do cursor dos provedores de dados. Como resultado, o usuário percebe uma funcionalidade relativamente uniforme de todos os provedores de dados.

O Cursor Service disponibiliza propriedades dinâmicas e melhora o comportamento de determinados métodos. Por exemplo, a propriedade dinâmica [Optimize](optimize-property-dynamic-ado.md) permite a criação de índices temporários para facilitar determinadas operações, como o método [Find](find-method-ado.md).

O Cursor Service permite o suporte para atualização em lote em todos os casos. Além disso, ele simula tipos de cursores mais avançados, como os cursores dinâmicos, quando um provedor de dados pode oferecer suporte apenas a cursores com menos recursos, como os cursores estáticos.

## <a name="keyword"></a>Palavra-chave

Para invocar esse componente de serviço, defina a propriedade [CursorLocation](cursorlocation-property-ado.md) dos objetos [Recordset](recordset-object-ado.md) ou [Connection](connection-object-ado.md) como **adUseClient**.

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Propriedades dinâmicas

Quando o Cursor Service para OLE DB é invocado, as propriedades dinâmicas listadas abaixo são adicionadas à coleção [Properties](properties-collection-ado.md) do objeto **Recordset**. A lista completa de propriedades dinâmicas dos objetos **Connection** e **Recordset** é fornecida no [Índice de Propriedades Dinâmicas do ADO](ado-dynamic-property-index.md). Os nomes das propriedades associadas do OLE DB, quando adequados, são incluídos entre parênteses após o nome da propriedade do ADO.

As alterações em algumas propriedades dinâmicas não são visíveis para a fonte de dados de base depois que o Cursor Service é invocado. Por exemplo, a definição da propriedade  *Command Time out* de um **Recordset** não ficará visível para o provedor de dados de base.

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

Se o seu aplicativo exige o Cursor Service, mas você precisa definir propriedades dinâmicas no provedor de base, defina as propriedades antes de chamar o Cursor Service. As definições de propriedades de objetos de comando sempre são passadas para o provedor de dados de base, independentemente do local do cursor. Portanto, você também pode usar um objeto de comando para definir as propriedades a qualquer momento.

> [!NOTE]
> [!OBSERVAçãO] O serviço de cursor não oferece suporte à propriedade dinâmica DBPROP_SERVERDATAONINSERT, mesmo que o provedor de dados de base ofereça esse suporte.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da Propriedade</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Auto Recalc<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>Nos conjuntos de registros criados com o Data Shaping Service, esse valor indica com que frequência as colunas calculadas e agregadas serão calculadas. O padrão (valor=1) é recalcular sempre que o Data Shaping Service determinar que os valores foram alterados. Se o valor for 0, as colunas calculadas ou agregadas serão calculadas somente durante a construção inicial da hierarquia.</p></td>
</tr>
<tr class="even">
<td><p>Batch Size<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>Indica o número de instruções de atualização que podem ser colocadas em lote antes de serem enviadas para o repositório de dados. Quanto maior for o número de instruções em um lote, menos ciclos de armazenamento de dados serão necessários.</p></td>
</tr>
<tr class="odd">
<td><p>Cache Child Rows<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>Nos conjuntos de registros criados com o Data Shaping Service, este valor indica se os conjuntos de registros filhos serão armazenados em um cache para utilização posterior.</p></td>
</tr>
<tr class="even">
<td><p>Cursor Engine Version<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>Indica a versão do Cursor Service que está sendo utilizada.</p></td>
</tr>
<tr class="odd">
<td><p>Maintain Change Status<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>Indica o texto do comando utilizado para sincronizar novamente uma ou mais linhas em uma junção de várias tabelas.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Otimização</a></p></td>
<td><p>Indica se um índice deverá ser criado. Se for definido como <strong>True</strong>, autorizará a criação temporária de índices para melhorar a execução de determinadas operações.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Indica o nome do <strong>Recordset</strong>. Pode ser referenciado nos comandos atuais ou de data shaping subsequentes.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Indica uma sequência de comandos personalizada utilizada pelo método <a href="resync-method-ado.md">Resync</a> quando a propriedade <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> estiver em vigor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></p></td>
<td><p>Indica o nome do banco de dados que contém a tabela referenciada na propriedade <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></p></td>
<td><p>Indica o nome do proprietário da tabela referenciada na propriedade <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></p></td>
<td><p>Indica o nome da tabela única criada em um <strong>Recordset</strong> a partir de várias tabelas que podem ter sido modificadas por inserções, atualizações ou exclusões.</p></td>
</tr>
<tr class="even">
<td><p>Update Criteria<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>Indica quais campos da cláusula <strong>WHERE</strong> serão utilizados para lidar com colisões que ocorram durante uma atualização.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p>Indica se o método <strong>Resync</strong> será invocado implicitamente após o método <a href="updatebatch-method-ado.md">UpdateBatch</a> (e seu comportamento) quando a propriedade <strong>Unique Table</strong> estiver em vigor.</p></td>
</tr>
</tbody>
</table>


Você também pode definir ou recuperar uma propriedade dinâmica especificando o seu nome como índice da coleção **Properties**. Isso, por exemplo, recupera e imprime o valor atual da propriedade dinâmica [Optimize](optimize-property-dynamic-ado.md) e depois define um novo valor:

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Comportamento de propriedades internas

O Cursor Service para OLE DB também afeta o comportamento de determinadas propriedades internas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da Propriedade</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Complementa os tipos de cursores que estão disponíveis para um <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Complementa os tipos de bloqueios que estão disponíveis para um <strong>Recordset</strong>. Habilita atualizações em lote.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Especifica um ou mais nomes de campos com base nos quais o <strong>Recordset</strong> será classificado e se cada campo será classificado em ordem crescente ou decrescente.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Comportamento de métodos

O Cursor Service para OLE DB habilita ou afeta o comportamento do método [Append](append-method-ado.md) do objeto [Field](field-object-ado.md); e dos métodos  [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) e [Save](save-method-ado.md) do objeto **Recordset**.

