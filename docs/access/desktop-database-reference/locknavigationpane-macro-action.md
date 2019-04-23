---
title: Ação da macro BloquearPainelDeNavegação
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289868"
---
# <a name="locknavigationpane-macro-action"></a>Ação da macro BloquearPainelDeNavegação


**Aplica-se ao:** Access 2013, Office 2013

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

O bloqueio do Painel de Navegação impede que você exclua os objetos de banco de dados ou recorte-os para a área de transferência. Ele *não* impede que você execute alguma das operações a seguir:

  - Copiar objetos de banco de dados para a área de transferência

  - Colar objetos de banco de dados da área de transferência

  - Exibir ou ocultar o Painel de Navegação

  - Selecionar diferentes esquemas de organização do Painel de Navegação

  - Mostrar ou ocultar seções do Painel de Navegação

Para executar a ação **BloquearPainelDeNavegação** em um módulo do VBA, use o método **LockNavigationPane** do objeto **DoCmd**.

