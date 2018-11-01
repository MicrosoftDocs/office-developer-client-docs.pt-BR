---
title: Ação de macro DefinirCampo
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1be405402c5f410c892c2dd8904133e09039351a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869498"
---
# <a name="setfield-macro-action"></a>Ação de macro DefinirCampo


**Aplica-se a**: Access 2013, o Office 2013

A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo.


> [!NOTE]
> <P>[!OBSERVAçãO] A ação <STRONG>DefinirCampo</STRONG> está disponível somente em Macros de Dados.</P>



## <a name="setting"></a>Configuração

A ação **DefinirCampo** tem os seguintes listados na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
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

