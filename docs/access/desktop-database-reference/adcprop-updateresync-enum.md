---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 056e68456b3f5bcf30768b0a5a616467c8271a5a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861404"
---
# <a name="adcpropupdateresyncenum"></a>ADCPROP\_UPDATERESYNC\_ENUM

**Aplica-se a**: Access 2013 | Office 2013

Especifica se o método [UpdateBatch](updatebatch-method-ado.md) é seguido por uma operação do método [Resync](resync-method-ado.md) implícita e, se for, especifica o escopo dessa operação.

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
<td><p><strong>adResyncAll</strong></p></td>
<td><p>15</p></td>
<td><p>Chama <strong>Resync</strong> com o valor combinado de todos os outros membros ADCPROP_UPDATERESYNC_ENUM.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1</p></td>
<td><p>Padrão. Tenta recuperar o novo valor de identidade para as colunas que são automaticamente incrementadas ou geradas pela fonte de dados, como os campos AutoNumber do Microsoft Jet ou as colunas Identity do Microsoft SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2</p></td>
<td><p>Chama <strong>Resync</strong> para todas as linhas nas quais a operação de atualização ou exclusão falhou devido a um conflito de simultaneidade.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8</p></td>
<td><p>Chama <strong>Resync</strong> para todas as linhas inseridas com êxito. No entanto, os valores da coluna AutoIncrement não estejam sincronizados. Em vez disso, o conteúdo de linhas recém-inseridas estejam sincronizado com base no valor da chave primária existente. Se a chave primária é um valor de incremento automático, <strong>Resync</strong> não irá recuperar o conteúdo da linha pretendido. Para incrementar automaticamente os valores de chave primária AutoIncrement, chame <strong>UpdateBatch</strong> com de <strong>adResyncAutoIncrement</strong> o valor combinado + <strong>adResyncInserts</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p>Não chama <strong>Resync</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4</p></td>
<td><p>Chama <strong>Resync</strong> para todas as linhas atualizadas com êxito.</p></td>
</tr>
</tbody>
</table>

