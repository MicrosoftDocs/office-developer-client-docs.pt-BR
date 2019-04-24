---
title: Determinando o modo de edição
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5b62bc282a99472d0e7399ee9f3dd9d0648f0c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293914"
---
# <a name="determining-edit-mode"></a>Determinando o modo de edição


**Aplica-se ao:** Access 2013, Office 2013

O ADO mantém um buffer de edição associado ao registro atual. A propriedade **EditMode** indica se foram feitas alterações nesse buffer ou se um novo registro foi criado. Use **EditMode** para determinar o status de edição do registro atual. Você pode fazer um teste para saber se há alterações pendentes, caso um processo de edição tenha sido interrompido, e determinar se é necessário usar o método **Update** ou **CancelUpdate**.

**EditMode** retorna uma das constantes **EditModeEnum**, que são listadas na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adEditNone</strong></p></td>
<td><p>Indica que nenhuma operação de edição está em andamento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>Indica que os dados no registro atual foram modificados, mas não foram salvos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>Indica que o método <strong>AddNew</strong> foi chamado e que o registro atual no buffer de cópia é novo e não foi salvo no banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>Indica que o registro atual foi excluído.</p></td>
</tr>
</tbody>
</table>


**EditMode** pode retornar um valor válido somente se houver um registro atual. **EditMode** retornará um erro se **BOF** ou **EOF** for **True** ou se o registro atual tiver sido excluído.

