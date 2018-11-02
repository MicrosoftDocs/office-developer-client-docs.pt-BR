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
ms.openlocfilehash: f22d1a30a2dc7de003510f54d64fcafc9f0f7878
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920204"
---
# <a name="workflowtasks-macro-action"></a>Ação da macro TarefasDeFluxoDeTrabalho


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **TarefasDeFluxoDeTrabalho** para exibir a caixa de diálogo **Tarefa de Fluxo de Trabalho**.

## <a name="setting"></a>Configuração

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
<td><p>A posição do item na lista do Microsoft SharePoint Foundation, começando com <strong>1</strong> para o primeiro item na lista, <strong>2</strong> para o segundo item, e assim por diante. Você também pode inserir uma expressão para este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

  - A ação **TarefasDeFluxoDeTrabalho** abre a caixa de diálogo **Tarefas de Fluxo de Trabalho**. Essa caixa de diálogo exibe todas as tarefas disponíveis para o item especificado. Um fluxo de trabalho deve ser definido para a lista no SharePoint Foundation.

  - A ação **TarefasDeFluxoDeTrabalho** pode ser usada somente depois de uma lista vinculada do SharePoint Foundation ter sido aberta e selecionada. Para abrir e selecionar a lista vinculada, use a ação **AbrirTabela**. Se a lista já estiver aberta, use a ação **SelecionarObjeto** para selecioná-la.

  - A ação **TarefasDeFluxoDeTrabalho** tem o mesmo efeito de clicar com o botão direito do mouse em qualquer célula de uma lista vinculada do SharePoint Foundation enquanto ela está aberta no modo de folha de dados, apontar para **Fluxo de Trabalho** e clicar em **Tarefas de Fluxo de Trabalho**.

  - Para executar a ação **TarefasDeFluxoDeTrabalho** em um módulo do VBA, use o método **WorkflowTasks** do objeto **DoCmd**.

