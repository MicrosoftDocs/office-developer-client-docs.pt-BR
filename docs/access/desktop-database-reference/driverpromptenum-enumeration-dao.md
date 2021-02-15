---
title: Enumeração driverPromptEnum (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293662"
---
# <a name="driverpromptenum-enumeration-dao"></a>Enumeração driverPromptEnum (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Especifica se e quando o usuário deve ser solicitado a estabelecer uma conexão.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbDriverComplete</p></td>
<td><p>0</p></td>
<td><p>Se a sequência de conexão fornecida incluir a palavra-chave DSN, o gerenciador de driver utilizará a sequência de caracteres, conforme fornecida na conexão. Caso contrário, seu comportamento será o mesmo de quando <strong>dbDriverPrompt</strong> é especificado.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverCompleteRequired</p></td>
<td><p>3 </p></td>
<td><p>(Padrão) Comporta-se como <strong>dbDriverComplete</strong>, exceto pelo fato de que o driver desabilita os controles de quaisquer informações que não sejam necessárias para concluir a conexão.</p></td>
</tr>
<tr class="odd">
<td><p>dbDriverNoPrompt</p></td>
<td><p>1 </p></td>
<td><p>O gerenciador de driver usa a sequência de conexão fornecida na conexão. Se não forem fornecidas informações suficientes, será retornado um erro interceptável.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverPrompt</p></td>
<td><p>2 </p></td>
<td><p>O gerenciador de driver exibe a caixa de diálogo <strong>Fontes de Dados ODBC</strong>. A sequência de conexão usada para estabelecer a conexão é construída a partir do DSN (nome da fonte de dados) selecionado e é completada pelo usuário por meio das caixas de diálogo.</p></td>
</tr>
</tbody>
</table>

