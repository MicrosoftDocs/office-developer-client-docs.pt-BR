---
title: Linha User-defined Cells (Seção User-defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Contém o valor e o prompt descritivo para qualquer célula definida pelo usuário na solução. Uma forma contém uma linha User-defined Cells para cada par de célula Value/Prompt definida pelo usuário.
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337181"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a><span data-ttu-id="b888f-104">Linha User-defined Cells (Seção User-defined Cells)</span><span class="sxs-lookup"><span data-stu-id="b888f-104">User-defined Cells Row (User-defined Cells Section)</span></span>

<span data-ttu-id="b888f-p102">Contém o valor e o prompt descritivo para qualquer célula definida pelo usuário na solução. Uma forma contém uma linha User-defined Cells para cada par de célula Value/Prompt definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b888f-p102">Contains the value and descriptive prompt for any user-defined cells in your solution. A shape contains one User-defined Cells row for each user-defined Value/Prompt cell pair.</span></span>
  
<span data-ttu-id="b888f-107">As linhas User-defined Cells são denominadas User.</span><span class="sxs-lookup"><span data-stu-id="b888f-107">User-defined Cells rows are named User.</span></span> <span data-ttu-id="b888f-108">*nome* e contém as células a seguir.</span><span class="sxs-lookup"><span data-stu-id="b888f-108">*name*  and contain the following cells.</span></span> <span data-ttu-id="b888f-109">Para obter mais detalhes, consulte os tópicos específicos das células.</span><span class="sxs-lookup"><span data-stu-id="b888f-109">For more details, see the specific cell topics.</span></span> 
  
|<span data-ttu-id="b888f-110">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b888f-110">**Cell**</span></span>|<span data-ttu-id="b888f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b888f-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b888f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b888f-112">Value</span></span>](value-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="b888f-113">Especifica um valor para a célula definida pelo usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="b888f-113">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |
|[<span data-ttu-id="b888f-114">Prompt</span><span class="sxs-lookup"><span data-stu-id="b888f-114">Prompt</span></span>](prompt-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="b888f-115">Especifica um comentário ou prompt descritivo para a célula definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b888f-115">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b888f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b888f-116">Remarks</span></span>

<span data-ttu-id="b888f-p104">Células definidas pelo usuário podem ser usadas para inserir fórmulas ou constantes que são referenciadas por outras células ou outros complementos. Os valores nas células definidas pelo usuário são portáteis, isto é, se uma forma que faz referência a uma célula definida pelo usuário em uma forma for copiada para outra forma que não tenha a mesma célula definida pelo usuário, a célula será adicionada à forma.</span><span class="sxs-lookup"><span data-stu-id="b888f-p104">User-defined cells can be used for entering formulas or constants that are referred to by other cells or add-ons. Values in user-defined cells are portable, that is, if a shape that refers to a user-defined cell in one shape is copied to another shape that does not have the same user-defined cell, the cell is added to the shape.</span></span>
  
 <span data-ttu-id="b888f-119">É possível adicionar tantas linhas User.</span><span class="sxs-lookup"><span data-stu-id="b888f-119">You can add as many User.</span></span>  <span data-ttu-id="b888f-120">*nomear* linhas conforme necessário, atribuir nomes significativos às linhas e definir valores de célula.</span><span class="sxs-lookup"><span data-stu-id="b888f-120">*name*  rows as you need, assign meaningful names to the rows, and set cell values.</span></span> <span data-ttu-id="b888f-121">Para adicionar uma linha a uma seção User-defined Cells existente, clique com o botão direito do mouse em uma linha e clique em **Inserir Linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="b888f-121">To add a row to an existing User-defined Cells section, right-click a row and click **Insert Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="b888f-122">É possível fazer referência a essas células pelo nome da linha, exibido na janela ShapeSheet em texto vermelho.</span><span class="sxs-lookup"><span data-stu-id="b888f-122">You can reference these cells by their row name, which appears in a ShapeSheet window in red text.</span></span> <span data-ttu-id="b888f-123">Para atribuir nomes significativos às linhas User.</span><span class="sxs-lookup"><span data-stu-id="b888f-123">To assign meaningful names to User.</span></span> <span data-ttu-id="b888f-124">*nomear* linhas, clique na linha e digite um nome como *deslocamento* , por exemplo, para criar o nome da linha user. Offset.</span><span class="sxs-lookup"><span data-stu-id="b888f-124">*name*  rows, click the row, and then type a name such as  *Offset*  , for example, to create the row name User.Offset.</span></span> <span data-ttu-id="b888f-125">Você pode fazer referência à célula Prompt usando User.Offset.Prompt.</span><span class="sxs-lookup"><span data-stu-id="b888f-125">You can then reference the Prompt cell using User.Offset.Prompt.</span></span> 
  
<span data-ttu-id="b888f-126">O nome de linha inserido deve ser único na seção.</span><span class="sxs-lookup"><span data-stu-id="b888f-126">The row name you enter must be unique within the section.</span></span>
  

