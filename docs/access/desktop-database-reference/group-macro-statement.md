---
title: Instrução de macro Grupo
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35f9ad1d445dbddaa5487e28da60b9202a72dae1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879848"
---
# <a name="group-macro-statement"></a>Instrução de macro Grupo


**Aplica-se a**: Access 2013, o Office 2013

A instrução **grupo** permite que você especifique um bloco de ações em uma macro que você pode expandir ou recolher.

## <a name="setting"></a>Configuração

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

