---
title: ConnectModeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295692"
---
# <a name="connectmodeenum"></a>ConnectModeEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica as permissões disponíveis para modificar os dados em uma [Connection](connection-object-ado.md), abrir um [Record](record-object-ado.md) ou especificar os valores para a propriedade [Mode](mode-property-ado.md) dos objetos **Record** e [Stream](stream-object-ado.md).

<br/>

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
<td><p><strong>adModeRead</strong></p></td>
<td><p>1</p></td>
<td><p>Indica permissões somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeReadWrite</strong></p></td>
<td><p>3D</p></td>
<td><p>Indica permissões de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeRecursive</strong></p></td>
<td><p>0x400000</p></td>
<td><p>Usado em conjunto com os outros valores de <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>ou <strong>adModeShareDenyRead</strong>) para propagar restrições de compartilhamento para todos os subregistros do <strong>registro</strong>atual. Não terá efeito se o <strong>Registro</strong> não tiver filhos.</p><p>Um erro de tempo de execução será gerado se for usado apenas com o <strong>adModeShareDenyNone</strong>. No entanto, pode ser usado com <strong>adModeShareDenyNone</strong> quando combinado a outros valores. Por exemplo, você pode usar &quot;o <strong>adModeRead</strong> ou o <strong>adModeShareDenyNone</strong> ou o <strong>adModeRecursive</strong>&quot;.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyNone</strong></p></td>
<td><p>dezesseis</p></td>
<td><p>Permite que outras pessoas estabeleçam uma conexão com quaisquer permissões. Não pode ser negado a terceiros acesso de leitura nem de gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareDenyRead</strong></p></td>
<td><p>quatro</p></td>
<td><p>Impede que outras pessoas estabeleçam uma conexão com permissões de leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeShareDenyWrite</strong></p></td>
<td><p>8</p></td>
<td><p>Impede que outras pessoas estabeleçam uma conexão com permissões de gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeShareExclusive</strong></p></td>
<td><p>3,6</p></td>
<td><p>Impede que outras pessoas estabeleçam uma conexão.</p></td>
</tr>
<tr class="even">
<td><p><strong>adModeUnknown</strong></p></td>
<td><p>,0</p></td>
<td><p>Padrão. Indica que as permissões ainda não foram definidas ou não podem ser determinadas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adModeWrite</strong></p></td>
<td><p>duas</p></td>
<td><p>Indica permissões de gravação apenas.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. ConnectMode. READ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. READWRITE</p></td>
</tr>
<tr class="odd">
<td><p>(Não há nenhum equivalente a AdoEnums.ConnectMode.RECURSIVE)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. SHAREDENYNONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectMode. SHAREDENYREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. SHAREDENYWRITE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectMode. SHAREEXCLUSIVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. ConnectMode. UNKNOWN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. ConnectMode. WRITE</p></td>
</tr>
</tbody>
</table>

