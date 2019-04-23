---
title: Instrução ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280422"
---
# <a name="add-user-statement-microsoft-access-sql"></a>Instrução ADD USER (Microsoft Access SQL)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um ou vários *usuários* existentes em um *grupo* existente.

## <a name="syntax"></a>Sintaxe

Adicionar *usuário*\[, *usuário*,... \] Para *Agrupar*

A instrução ADD USER possui as seguintes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>usuário</em></p></td>
<td><p>O nome de um usuário a ser adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
<tr class="even">
<td><p><em>grupo</em></p></td>
<td><p>O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Depois que um *usuário* tiver sido adicionado a um *grupo*, o *usuário* terá todas as permissões concedidas ao *grupo*.

