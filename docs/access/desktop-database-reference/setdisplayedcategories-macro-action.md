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
ms.openlocfilehash: 985630f65508f7fca37de24f93649c8cf6047180
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920316"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="4109d-102">Ação da macro DefinirCategoriasExibidas</span><span class="sxs-lookup"><span data-stu-id="4109d-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="4109d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4109d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4109d-p101">Você pode usar a ação **DefinirCategoriasExibidas** para especificar quais categorias serão exibidas em **Navegar para Categoria** na barra de título do Painel de Navegação. Por exemplo, para que os usuários não possam mudar o Painel de Navegação para exibir objetos classificados por **Data da Criação**, use essa ação para ocultar essa opção na lista suspensa da barra de título.</span><span class="sxs-lookup"><span data-stu-id="4109d-p101">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="4109d-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="4109d-106">Setting</span></span>

<span data-ttu-id="4109d-107">A ação **DefinirCategoriasExibidas** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4109d-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4109d-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="4109d-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4109d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4109d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4109d-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="4109d-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="4109d-p102">Selecione <strong>Sim</strong> para mostrar a(s) categoria(s). Selecione <strong>Não</strong> para ocultá-la(s).</span><span class="sxs-lookup"><span data-stu-id="4109d-p102">Select <strong>Yes</strong> to show the category or categories. Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4109d-113"><strong>Category</strong></span><span class="sxs-lookup"><span data-stu-id="4109d-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="4109d-p103">Digite ou selecione o nome da categoria que você deseja mostrar ou ocultar. Deixe em branco para mostrar ou ocultar todas as categorias.</span><span class="sxs-lookup"><span data-stu-id="4109d-p103">Enter or select the name of the category you want to show or hide. Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4109d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4109d-116">Remarks</span></span>

  - <span data-ttu-id="4109d-p104">A legenda da barra de título do Painel de Navegação indica o filtro que está atualmente ativo, caso haja algum filtro. Clique em qualquer lugar da barra para exibir a lista suspensa. Os itens que essa macro controla estão listados em **Navegar para Categoria**.</span><span class="sxs-lookup"><span data-stu-id="4109d-p104">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active. Click anywhere in the bar to display the drop-down list. The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="4109d-p105">Essa ação apenas habilita ou desabilita a exibição das categorias especificadas; ela não executa a alternância de exibição do Painel de Navegação. Por exemplo, se você estiver exibindo objetos classificados por **Data de Criação** e usar a ação **DefinirCategoriasExibidas** para desabilitar a opção **Data de Criação**, o Access não alternará a categoria no Painel de Navegação.</span><span class="sxs-lookup"><span data-stu-id="4109d-p105">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="4109d-122">Para executar a ação **DefinirCategoriasExibidas** em um módulo do VBA, use o método **SetDisplayedCategories** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4109d-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

