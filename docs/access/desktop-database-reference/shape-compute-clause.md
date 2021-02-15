---
title: Cláusula de cálculo de forma
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306451"
---
# <a name="shape-compute-clause"></a>Cláusula de cálculo de forma

**Aplica-se ao:** Access 2013, Office 2013

Uma cláusula COMPUTE de forma gera um **Recordset** pai, cujas colunas consistem em uma referência ao **Recordset** filho; colunas opcionais cujo conteúdo são colunas de capítulo, colunas novas ou colunas calculadas, ou o resultado da execução de funções agregadas no **Recordset** filho ou em um **Recordset** com formato anterior; e todas as colunas do **Recordset** filho listado na cláusula BY opcional.

## <a name="syntax"></a>Sintaxe

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>Descrição

As partes dessa cláusula são as seguintes:

- *child-command*

  - Consiste em um dos itens a seguir:
    
    - Um comando de consulta entre chaves ("{}") que retorna um objeto **Recordset** filho. O comando é emitido para o provedor de dados subjacente, e sua sintaxe depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.
    
    - O nome de um **Recordset** com formato existente.
    
    - Um outro comando shape.
    
    - A palavra-chave TABLE, seguida do nome de uma tabela no provedor de dados.

- *child-alias*

  - Um alias usado para se referir ao **Recordset** retornado por *child-command.* O *child-alias* é necessário na lista de colunas na cláusula COMPUTE e define a relação entre os objetos **Recordset** pai e filho.

- *appended-column-list*

  - Uma lista na qual cada elemento define uma coluna no pai gerado. Cada elemento consiste em uma coluna de capítulo, uma nova coluna, uma coluna calculada ou um valor resultante de uma função de agregação no **Recordset** filho.

- *grp-field-list*

  - Uma lista de colunas nos objetos **Recordset** pai e filho que especifica o modo de agrupamento das linhas no filho. Para cada coluna em *grp-field-list,* há uma coluna correspondente nos objetos **Recordset** pai e filho. Para cada linha no **Recordset** pai, são exibidos valores exclusivos nas colunas *grp-field-list*, e o **Recordset** filho referenciado pela linha pai consiste apenas em linhas filho cujas colunas *grp-field-list* têm os mesmos valores da linha pai.

Se a cláusula BY for incluída, as linhas do **Recordset** filho serão agrupadas com base nas colunas na cláusula COMPUTE. O **Recordset** pai conterá uma linha para cada grupo de linhas no **Recordset** filho.

Se a cláusula BY for omitida, todo o **Recordset** filho será tratado como um único grupo e o **Recordset** pai conterá exatamente uma linha. Essa linha fará referência a todo o **Recordset** filho. A omissão da cláusula BY permite calcular o "total geral" de agregados em todo o **Recordset** filho.

Por exemplo:

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Independentemente do modo de formação do **Recordset** pai (usando COMPUTE ou APPEND), ele conterá uma coluna de capítulo usada para relacioná-lo a um **Recordset** filho. Se você desejar, o **Recordset** pai também poderá conter colunas com agregados (SUM, MIN, MAX etc.) nas linhas filho. Os objetos **Recordset** pai e filho podem conter colunas com uma expressão na linha de **Recordset**, bem como colunas novas e inicialmente vazias.

## <a name="operation"></a>Operation

*child-command* é emitido para o provedor, que retorna um **Recordset** filho.

A cláusula COMPUTE especifica as colunas do **Recordset** pai, que pode ser uma referência ao **Recordset** filho, um ou mais agregados, uma expressão calculada ou novas colunas. Se houver uma cláusula BY, as colunas definidas por ela também serão acrescentadas ao **Recordset** pai. A cláusula BY especifica o modo de agrupamento do **Recordset** filho.

Por exemplo, suponha que você tenha uma tabela  Demografia  contendo os campos Estado, Cidade e População (os números referentes à população são apenas para fins ilustrativos).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Cidade</p></th>
<th><p>População</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>OU</p></td>
<td><p>Medford</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="odd">
<td><p>OU</p></td>
<td><p>Portland</p></td>
<td><p>400.000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>Los Angeles</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="odd">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600.000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Rúma</p></td>
<td><p>US$ 500.000</p></td>
</tr>
<tr class="odd">
<td><p>OU</p></td>
<td><p>Corção</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>


Agora, emita este comando shape:

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

O comando abre um **Recordset** com formato de dois níveis. O nível pai é um **Recordset** gerado com uma coluna agregada (SUM(rs.population), uma coluna que faz referência ao **Recordset** filho (rs) e uma coluna para agrupar o **Recordset** filho (estado). O nível filho é o **Recordset** retornado pelo comando de consulta (), uma coluna que faz referência ao **Recordset** filho (rs) e uma coluna para agrupar o **Recordset** filho (estado). O nível filho é o **Recordset retornado** pelo comando de consulta (seleção \* de demografia).

As linhas de detalhes do **Recordset** filho serão agrupadas por estado, mas sem nenhuma ordem específica, ou seja, os grupos não estarão em ordem alfabética ou numérica. Se desejar ordenar o **Recordset** pai, você poderá usar o método **Sort** de **Recordset** para ordenar o **Recordset** pai.

Agora, você pode navegar pelo **Recordset** pai aberto e acessar os objetos **Recordset** filho de detalhes. Para obter mais informações, consulte [Acessando linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md).

**Conjuntos de registros de detalhes pai e filho resultantes**

**Pai**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SUM (rs.Population)</p></th>
<th><p>rs</p></th>
<th><p>Estado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Referência ao filho1</p></td>
<td><p>CA</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Referência ao filho2</p></td>
<td><p>WA</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
<td><p>Referência ao filho3</p></td>
<td><p>OU</p></td>
</tr>
</tbody>
</table>


**Child1**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Cidade</p></th>
<th><p>População</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CA</p></td>
<td><p>Los Angeles</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>San Diego</p></td>
<td><p>600.000</p></td>
</tr>
</tbody>
</table>


**Child2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Cidade</p></th>
<th><p>População</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Rúma</p></td>
<td><p>US$ 500.000</p></td>
</tr>
</tbody>
</table>


**Child3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Estado</p></th>
<th><p>Cidade</p></th>
<th><p>População</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>OU</p></td>
<td><p>Medford</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="even">
<td><p>OU</p></td>
<td><p>Portland</p></td>
<td><p>400.000</p></td>
</tr>
<tr class="odd">
<td><p>OU</p></td>
<td><p>Corção</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>

