---
title: Ação de macro BloquearPainelDeNavegação
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2db34ee9ea56c5fcb4c5aff6afa57c3f59d1f17c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870328"
---
# <a name="locknavigationpane-macro-action"></a>Ação de macro BloquearPainelDeNavegação


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **BloquearPainelDeNavegação** para impedir que os usuários excluam objetos de banco de dados exibidos no Painel de Navegação.

## <a name="setting"></a>Configuração

A ação **BloquearPainelDeNavegação** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Lock</strong></p></td>
<td><p>Selecione <strong>Sim</strong> para bloquear o Painel de Navegação ou <strong>Não</strong> para desbloqueá-lo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O bloqueio do Painel de Navegação impede que você exclua os objetos de banco de dados ou recorte-os para a área de transferência. Ela faz *não* impede que você realize qualquer uma das seguintes operações:

  - Copiar objetos de banco de dados para a área de transferência

  - Colar objetos de banco de dados da área de transferência

  - Exibir ou ocultar o Painel de Navegação

  - Selecionar diferentes esquemas de organização do Painel de Navegação

  - Mostrar ou ocultar seções do Painel de Navegação

Para executar a ação **BloquearPainelDeNavegação** em um módulo do VBA, use o método **LockNavigationPane** do objeto **DoCmd**.

