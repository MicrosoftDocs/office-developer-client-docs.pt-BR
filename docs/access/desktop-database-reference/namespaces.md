---
title: Namespaces (referência de banco de dados da área de trabalho do Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef37f04ec6824cedf773cb72751b2364d2b3edf8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876558"
---
# <a name="namespaces"></a>Namespaces


**Aplica-se a**: Access 2013, o Office 2013

## <a name="namespaces"></a>Espaços de nome

O formato de persistência do XML no ADO usa estes espaços de nome.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefixo</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Refere-se para o &quot;dados XML&quot; namespace que contém os elementos e atributos que definem o esquema do <strong>Recordset</strong>atual.</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>Refere-se à especificação das definições do tipo de dados.</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
<td><p>Refere-se ao namespace que contém os elementos e os atributos específicos das propriedades e dos atributos do <strong>Recordset</strong> do ADO.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Refere-se ao esquema do conjunto de linhas atual.</p></td>
</tr>
</tbody>
</table>


Um cliente não deve adicionar suas próprias marcas a esses espaços de nome, conforme definido pela especificação. Por exemplo, um cliente não deve definir um namespace como "urn:schemas-microsoft-com:rowset" e gravar algo como "rs:MyOwnTag." Para saber mais sobre os espaços de nome, consulte [Espaços de nome XML](https://www.w3.org/tr/xml-names/).


> [!NOTE]
> <P>[!OBSERVAçãO] O código da marca do esquema deve ser "RowsetSchema" e o namespace usado para fazer referência ao esquema do conjunto de linhas atual deve apontar para "#RowsetSchema".</P>



Observe que o prefixo do namespace, aquela parte à direita dos dois-pontos e à esquerda do sinal de igual, é arbitrário.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

O usuário pode defini-lo como qualquer nome, contanto que esse nome seja usado de forma consistente no documento XML inteiro. O ADO sempre grava "s", "rs", "dt" e "z", mas esses nomes de prefixo não estão embutidos em código no componente de carga.

## <a name="namespaces"></a>Espaços de nome

O formato de persistência do XML no ADO usa estes espaços de nome.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefixo</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Refere-se para o &quot;dados XML&quot; namespace que contém os elementos e atributos que definem o esquema do <strong>Recordset</strong>atual.</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>Refere-se à especificação das definições do tipo de dados.</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
<td><p>Refere-se ao namespace que contém os elementos e os atributos específicos das propriedades e dos atributos do <strong>Recordset</strong> do ADO.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Refere-se ao esquema do conjunto de linhas atual.</p></td>
</tr>
</tbody>
</table>


Um cliente não deve adicionar suas próprias marcas a esses espaços de nome, conforme definido pela especificação. Por exemplo, um cliente não deve definir um namespace como "urn:schemas-microsoft-com:rowset" e gravar algo como "rs:MyOwnTag." Para saber mais sobre os espaços de nome, consulte [Espaços de nome XML](https://www.w3.org/tr/xml-names/).


> [!NOTE]
> <P>[!OBSERVAçãO] O código da marca do esquema deve ser "RowsetSchema" e o namespace usado para fazer referência ao esquema do conjunto de linhas atual deve apontar para "#RowsetSchema".</P>



Observe que o prefixo do namespace, aquela parte à direita dos dois-pontos e à esquerda do sinal de igual, é arbitrário.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

O usuário pode defini-lo como qualquer nome, contanto que esse nome seja usado de forma consistente no documento XML inteiro. O ADO sempre grava "s", "rs", "dt" e "z", mas esses nomes de prefixo não estão embutidos em código no componente de carga.

