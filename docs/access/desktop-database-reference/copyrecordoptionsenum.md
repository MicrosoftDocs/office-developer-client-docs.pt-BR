---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3c3ddd8174a646bccd37cec758e85e17f4cdaec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882774"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum


**Aplica-se a**: Access 2013, o Office 2013

Especifica o comportamento do método [CopyRecord](copyrecord-method-ado.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adCopyAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Indica que o provedor de <em>Origem</em> tenta simular a cópia usando as operações de download e upload se esse método falhar devido a um <em>Destino</em> estar em um servidor diferente ou se for atendido pro um provedor diferente da <em>Origem</em>. Observe que a diferenciação dos recursos do provedor pode dificulta o desempenho ou ocasionar perda de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyNonRecursive</strong></p></td>
<td><p>2</p></td>
<td><p>Copia o diretório atual, mas nenhum dos seus subdiretórios, para o destino. A operação copiar não é recursiva.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCopyOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Sobregrava o arquivo ou diretório se o <em>Destino</em> apontar para um arquivo ou diretório existente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCopyUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Padrão. Executa a operação copiar padrão: A operação falha se o arquivo ou diretório de destino já existir e a operação fizer a cópia de maneira recursiva.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

