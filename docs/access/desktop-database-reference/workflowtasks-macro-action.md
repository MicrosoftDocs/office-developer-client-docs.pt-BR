---
title: Ação da macro TarefasDeFluxoDeTrabalho
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306003"
---
# <a name="workflowtasks-macro-action"></a>Ação da macro TarefasDeFluxoDeTrabalho


**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **TarefasDeFluxoDeTrabalho** para exibir a caixa de diálogo **Tarefa de Fluxo de Trabalho**.

## <a name="setting"></a>Setting

A ação **TarefasDeFluxoDeTrabalho** tem o argumento a seguir.

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
<td><p><strong>Número de registro</strong></p></td>
<td><p>A posição do item na lista do Microsoft SharePoint Foundation, começando com <strong>1</strong> para o primeiro item na lista, <strong>2</strong> para o segundo item e assim por diante. Você também pode inserir uma expressão para esse argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

  - A ação **TarefasDeFluxoDeTrabalho** abre a caixa de diálogo **Tarefas de Fluxo de Trabalho**. Essa caixa de diálogo exibe todas as tarefas disponíveis para o item especificado. Um fluxo de trabalho deve ser definido para a lista no SharePoint Foundation.

  - A ação **TarefasDeFluxoDeTrabalho** pode ser usada somente depois de uma lista vinculada do SharePoint Foundation ter sido aberta e selecionada. Para abrir e selecionar a lista vinculada, use a ação **AbrirTabela**. Se a lista já estiver aberta, use a ação **SelecionarObjeto** para selecioná-la.

  - A ação **TarefasDeFluxoDeTrabalho** tem o mesmo efeito de clicar com o botão direito do mouse em qualquer célula de uma lista vinculada do SharePoint Foundation enquanto ela está aberta no modo de folha de dados, apontar para **Fluxo de Trabalho** e clicar em **Tarefas de Fluxo de Trabalho**.

  - Para executar a ação **TarefasDeFluxoDeTrabalho** em um módulo do VBA, use o método **WorkflowTasks** do objeto **DoCmd**.

