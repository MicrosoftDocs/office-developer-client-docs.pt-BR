---
title: Ação da macro IniciarNovoFluxoDeTrabalho
TOCTitle: StartNewWorkflow Macro Action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c4c6d237ef24bea0c8509ac4ae0df00c4f30cec2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462936"
---
# <a name="startnewworkflow-macro-action"></a><span data-ttu-id="71a17-102">Ação da macro IniciarNovoFluxoDeTrabalho</span><span class="sxs-lookup"><span data-stu-id="71a17-102">StartNewWorkflow Macro Action</span></span>


<span data-ttu-id="71a17-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="71a17-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="71a17-104">Você pode usar a ação **IniciarNovoFluxoDeTrabalho** para iniciar um novo fluxo de trabalho para um item em uma lista vinculada do Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="71a17-104">You can use the **StartNewWorkflow** action to start a new workflow for an item in a linked Microsoft SharePoint Foundation list.</span></span>

## <a name="setting"></a><span data-ttu-id="71a17-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="71a17-105">Setting</span></span>

<span data-ttu-id="71a17-106">A ação **IniciarNovoFluxoDeTrabalho** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="71a17-106">The **StartNewWorkflow** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71a17-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="71a17-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="71a17-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="71a17-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71a17-109"><strong>Número de registro</strong></span><span class="sxs-lookup"><span data-stu-id="71a17-109"><strong>Record Number</strong></span></span></p></td>
<td><p><span data-ttu-id="71a17-110">A posição do item na lista do SharePoint Foundation, começando com <strong>1</strong> para o primeiro item na lista, <strong>2</strong> para o segundo item, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="71a17-110">The position of the item in the SharePoint Foundation list, starting with <strong>1</strong> for the first item in the list, <strong>2</strong> for the second item, and so on.</span></span> <span data-ttu-id="71a17-111">Você também pode inserir uma expressão para este argumento.</span><span class="sxs-lookup"><span data-stu-id="71a17-111">You can also enter an expression for this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="71a17-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="71a17-112">Remarks</span></span>

  - <span data-ttu-id="71a17-p102">A ação **IniciarNovoFluxoDeTrabalho** abre a caixa de diálogo **Iniciar Novo Fluxo de Trabalho**. Essa caixa de diálogo exibe todos os fluxos de trabalho disponíveis para o item especificado. Um fluxo de trabalho deve ser definido para a lista do SharePoint Foundation para que você possa iniciá-lo usando esta ação.</span><span class="sxs-lookup"><span data-stu-id="71a17-p102">The **StartNewWorkflow** action opens the **Start New Workflow** dialog box. This dialog box displays all workflows that are available for the specified item. A workflow must be defined for the list in SharePoint Foundation before you can start it using this action.</span></span>

  - <span data-ttu-id="71a17-p103">A ação **IniciarNovoFluxoDeTrabalho** pode ser usada somente depois de uma lista vinculada do SharePoint ter sido aberta e selecionada. Para abrir e selecionar a lista vinculada, use a ação **AbrirTabela**. Se a lista já estiver aberta, use a ação **SelecionarObjeto** para selecioná-la.</span><span class="sxs-lookup"><span data-stu-id="71a17-p103">The **StartNewWorkflow** action can only be used after a linked SharePoint list has been opened and selected. To open and select the linked list, use the **OpenTable** action. If the list is already open, use the **SelectObject** action to select it.</span></span>

  - <span data-ttu-id="71a17-119">A ação **IniciarNovoFluxoDeTrabalho** tem o mesmo efeito de clicar com o botão direito do mouse em qualquer célula de uma lista vinculada do SharePoint enquanto ela está aberta no modo Folha de Dados, apontar para **Fluxo de Trabalho** e clicar em **Iniciar Novo Fluxo de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="71a17-119">The **StartNewWorkflow** action has the same effect as right-clicking any cell in a linked SharePoint list while it is open in Datasheet view, pointing to **Workflow**, and then clicking **Start New Workflow**.</span></span>

  - <span data-ttu-id="71a17-120">Para executar a ação **IniciarNovoFluxoDeTrabalho** em um módulo do VBA, use o método **StartNewWorkflow** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="71a17-120">To run the **StartNewWorkflow** action in a VBA module, use the **StartNewWorkflow** method of the **DoCmd** object.</span></span>

