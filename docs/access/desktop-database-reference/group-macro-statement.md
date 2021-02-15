---
title: Instrução de macro Grupo
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292108"
---
# <a name="group-macro-statement"></a>Instrução de macro Grupo


**Aplica-se ao:** Access 2013, Office 2013

A **instrução Group** permite que você especifique um bloco de ações dentro de uma macro que pode ser expandida ou colapsado.

## <a name="setting"></a>Setting

A ação **Grupo** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Descrição</strong></p></td>
<td><p>Não</p></td>
<td><p>Uma cadeia de caracteres que aparece como o título de um grupo quando ele é recolhido.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A instrução **Grupo** não define uma região de uma macro que pode ser executada separadamente. Use a instrução **[Submacro](submacro-macro-statement.md)** para definir um conjunto de ações que podem ser executadas separadamente na janela **Designer de Macros**.

