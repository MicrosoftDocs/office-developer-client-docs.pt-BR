---
title: Ação da macro DefinirCampo
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314613"
---
# <a name="setfield-macro-action"></a>Ação da macro DefinirCampo

**Aplica-se ao:** Access 2013, Office 2013

A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo.

> [!NOTE]
> A ação **DefinirCampo** está disponível somente em Macros de Dados.

## <a name="setting"></a>Configuração

A ação **DefinirCampo** tem os seguintes listados na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nome</strong></p></td>
<td><p>Uma cadeia de caracteres que identifica o campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Valor</strong></p></td>
<td><p>Uma expressão que especifica o valor a ser atribuído ao campo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **DefinirCampo** não pode ser usada fora de um bloco de dados **[CriarRegistro](createrecord-data-block.md)** ou **[EditarRegistro](editrecord-data-block.md)**.

