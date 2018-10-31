---
title: Ação de macro ExibirPonteirodeAmpulheta
TOCTitle: DisplayHourglassPointer Macro Action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 725bb4530bffe9aeead327caa74cdba0798c181d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862650"
---
# <a name="displayhourglasspointer-macro-action"></a>Ação de macro ExibirPonteirodeAmpulheta


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **ExibirPonteirodeAmpulheta** para alterar o ponteiro do mouse para uma imagem de ampulheta (ou outro ícone escolhido) enquanto uma macro está em execução. Esta ação pode fornecer uma indicação visual de que a macro está em execução. Isso é especialmente útil quando uma ação de macro ou a própria macro leva muito tempo para ser executada.

## <a name="setting"></a>Configuração

A ação **ExibirPonteirodeAmpulheta** tem os seguintes argumentos.

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
<td><p><strong>Ampulheta Ativa</strong></p></td>
<td><p>Clique em <strong>Sim</strong> (exibir o ícone) ou <strong>Não</strong> (exibir o ponteiro do mouse normal) na caixa <strong>Ampulheta Ativa</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Sim</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Normalmente você usa esta ação se desativou o eco usando a ação **Eco**. Quando o eco está desativado, Access suspende as atualizações da tela até que a macro é concluída.

O Access redefine automaticamente o argumento **Ampulheta Ativa** como **Não** quando a execução da macro é concluída.

> [!NOTE]
> - No Microsoft Windows, este é o ícone definido para **Ocupado** na caixa de diálogo **Propriedades do Mouse** do Painel de Controle do Windows. O padrão para todos os sistemas operacionais Windows é um ícone de ampulheta animado.
> - É possível escolher outro ícone.

Para executar a ação **ExibirPonteirodeAmpulheta** em um módulo do VBA (Visual Basic for Applications), use o método **Ampulheta** do objeto **DoCmd**.

