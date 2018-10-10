---
title: Ação da macro TarefasDeFluxoDeTrabalho
TOCTitle: WorkflowTasks Macro Action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 29bd256c08a3b7c650609bc9b365436e5d332b8d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463308"
---
# <a name="workflowtasks-macro-action"></a><span data-ttu-id="6d6fa-102">Ação da macro TarefasDeFluxoDeTrabalho</span><span class="sxs-lookup"><span data-stu-id="6d6fa-102">WorkflowTasks Macro Action</span></span>


<span data-ttu-id="6d6fa-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d6fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6d6fa-104">Você pode usar a ação **TarefasDeFluxoDeTrabalho** para exibir a caixa de diálogo **Tarefa de Fluxo de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-104">You can use the **WorkflowTasks** action to display the **Workflow Task** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="6d6fa-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="6d6fa-105">Setting</span></span>

<span data-ttu-id="6d6fa-106">A ação **TarefasDeFluxoDeTrabalho** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-106">The **WorkflowTasks** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d6fa-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="6d6fa-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6d6fa-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d6fa-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d6fa-109"><strong>Número de registro</strong></span><span class="sxs-lookup"><span data-stu-id="6d6fa-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6fa-110">A posição do item na lista do Microsoft SharePoint Foundation, começando com <strong>1</strong> para o primeiro item na lista, <strong>2</strong> para o segundo item, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-110">The position of the item in the Microsoft SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="6d6fa-111">Você também pode inserir uma expressão para este argumento.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6d6fa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d6fa-112">Remarks</span></span>

  - <span data-ttu-id="6d6fa-p102">A ação **TarefasDeFluxoDeTrabalho** abre a caixa de diálogo **Tarefas de Fluxo de Trabalho**. Essa caixa de diálogo exibe todas as tarefas disponíveis para o item especificado. Um fluxo de trabalho deve ser definido para a lista no SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-p102">The **WorkflowTasks** action opens the **Workflow Tasks** dialog box. This dialog box displays all tasks that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation.</span></span>

  - <span data-ttu-id="6d6fa-p103">A ação **TarefasDeFluxoDeTrabalho** pode ser usada somente depois de uma lista vinculada do SharePoint Foundation ter sido aberta e selecionada. Para abrir e selecionar a lista vinculada, use a ação **AbrirTabela**. Se a lista já estiver aberta, use a ação **SelecionarObjeto** para selecioná-la.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-p103">The **WorkflowTasks** action can only be used after a linked SharePoint Foundation list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="6d6fa-119">A ação **TarefasDeFluxoDeTrabalho** tem o mesmo efeito de clicar com o botão direito do mouse em qualquer célula de uma lista vinculada do SharePoint Foundation enquanto ela está aberta no modo de folha de dados, apontar para **Fluxo de Trabalho** e clicar em **Tarefas de Fluxo de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-119">The **WorkflowTasks** action has the same effect as right-clicking any cell in a linked SharePoint Foundation list while it is open in datasheet view, pointing to **Workflow**, and then clicking **Workflow Tasks**.</span></span>

  - <span data-ttu-id="6d6fa-120">Para executar a ação **TarefasDeFluxoDeTrabalho** em um módulo do VBA, use o método **WorkflowTasks** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="6d6fa-120">To run the **WorkflowTasks** action in a VBA module, use the **WorkflowTasks** method of the **DoCmd** object.</span></span>

