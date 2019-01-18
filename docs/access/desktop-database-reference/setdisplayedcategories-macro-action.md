---
title: Ação da macro DefinirCategoriasExibidas
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711417"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="80c1c-102">Ação da macro DefinirCategoriasExibidas</span><span class="sxs-lookup"><span data-stu-id="80c1c-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="80c1c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="80c1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80c1c-p101">Você pode usar a ação **DefinirCategoriasExibidas** para especificar quais categorias serão exibidas em **Navegar para Categoria** na barra de título do Painel de Navegação. Por exemplo, para que os usuários não possam mudar o Painel de Navegação para exibir objetos classificados por **Data da Criação**, use essa ação para ocultar essa opção na lista suspensa da barra de título.</span><span class="sxs-lookup"><span data-stu-id="80c1c-p101">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="80c1c-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="80c1c-106">Setting</span></span>

<span data-ttu-id="80c1c-107">A ação **DefinirCategoriasExibidas** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="80c1c-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80c1c-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="80c1c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="80c1c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="80c1c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80c1c-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="80c1c-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="80c1c-p102">Selecione <strong>Sim</strong> para mostrar a(s) categoria(s). Selecione <strong>Não</strong> para ocultá-la(s).</span><span class="sxs-lookup"><span data-stu-id="80c1c-p102">Select <strong>Yes</strong> to show the category or categories. Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80c1c-113"><strong>Category</strong></span><span class="sxs-lookup"><span data-stu-id="80c1c-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="80c1c-p103">Digite ou selecione o nome da categoria que você deseja mostrar ou ocultar. Deixe em branco para mostrar ou ocultar todas as categorias.</span><span class="sxs-lookup"><span data-stu-id="80c1c-p103">Enter or select the name of the category you want to show or hide. Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="80c1c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="80c1c-116">Remarks</span></span>

  - <span data-ttu-id="80c1c-p104">A legenda da barra de título do Painel de Navegação indica o filtro que está atualmente ativo, caso haja algum filtro. Clique em qualquer lugar da barra para exibir a lista suspensa. Os itens que essa macro controla estão listados em **Navegar para Categoria**.</span><span class="sxs-lookup"><span data-stu-id="80c1c-p104">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active. Click anywhere in the bar to display the drop-down list. The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="80c1c-p105">Essa ação apenas habilita ou desabilita a exibição das categorias especificadas; ela não executa a alternância de exibição do Painel de Navegação. Por exemplo, se você estiver exibindo objetos classificados por **Data de Criação** e usar a ação **DefinirCategoriasExibidas** para desabilitar a opção **Data de Criação**, o Access não alternará a categoria no Painel de Navegação.</span><span class="sxs-lookup"><span data-stu-id="80c1c-p105">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="80c1c-122">Para executar a ação **DefinirCategoriasExibidas** em um módulo do VBA, use o método **SetDisplayedCategories** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="80c1c-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

