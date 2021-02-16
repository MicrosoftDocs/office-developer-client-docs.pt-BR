---
title: Célula PrintGrid (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Especifica se a grade será impressa ao imprimir a página de um documento.
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433203"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="a0aa6-103">Célula PrintGrid (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="a0aa6-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="a0aa6-104">Especifica se a grade será impressa ao imprimir a página de um documento.</span><span class="sxs-lookup"><span data-stu-id="a0aa6-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="a0aa6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a0aa6-105">**Value**</span></span>|<span data-ttu-id="a0aa6-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a0aa6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0aa6-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="a0aa6-107">TRUE</span></span>  <br/> |<span data-ttu-id="a0aa6-108">Mostra a grade ao imprimir a página.</span><span class="sxs-lookup"><span data-stu-id="a0aa6-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="a0aa6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a0aa6-109">FALSE</span></span>  <br/> |<span data-ttu-id="a0aa6-110">Não mostra a grade ao imprimir a página (o padrão).</span><span class="sxs-lookup"><span data-stu-id="a0aa6-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0aa6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0aa6-111">Remarks</span></span>

<span data-ttu-id="a0aa6-p101">Esse valor corresponde à caixa de seleção **Linhas de grade** da guia **Configurar Impressão** da caixa de diálogo **Configurar Página** (na guia **Design**, clique na seta **Configurar Página**). Fora a cor (a versão impressa é cinza), a grade impressa é idêntica à grade que você vê na janela de desenho do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="a0aa6-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="a0aa6-114">Você pode imprimir a grade página por página.</span><span class="sxs-lookup"><span data-stu-id="a0aa6-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="a0aa6-115">O estilo de grade também pode ser definido página por página na caixa  de diálogo  Grade de Régua (na guia Exibir, clique na seta Mostrar) quando uma página estiver ativa. **&amp;**</span><span class="sxs-lookup"><span data-stu-id="a0aa6-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="a0aa6-116">Para obter uma referência para a célula PrintGrid pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a0aa6-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0aa6-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a0aa6-117">Cell name:</span></span>  <br/> |<span data-ttu-id="a0aa6-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="a0aa6-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="a0aa6-119">Para obter uma referência para a célula PrintGrid pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a0aa6-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0aa6-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a0aa6-120">Section index:</span></span>  <br/> |<span data-ttu-id="a0aa6-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0aa6-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a0aa6-122">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="a0aa6-122">Row index:</span></span>  <br/> |<span data-ttu-id="a0aa6-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="a0aa6-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="a0aa6-124">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="a0aa6-124">Cell index:</span></span>  <br/> |<span data-ttu-id="a0aa6-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="a0aa6-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

