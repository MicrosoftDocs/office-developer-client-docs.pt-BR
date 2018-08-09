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
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772617"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="e2f68-103">Célula PrintGrid (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="e2f68-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="e2f68-104">Especifica se a grade será impressa ao imprimir a página de um documento.</span><span class="sxs-lookup"><span data-stu-id="e2f68-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="e2f68-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e2f68-105">**Value**</span></span>|<span data-ttu-id="e2f68-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e2f68-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2f68-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="e2f68-107">TRUE</span></span>  <br/> |<span data-ttu-id="e2f68-108">Mostra a grade ao imprimir a página.</span><span class="sxs-lookup"><span data-stu-id="e2f68-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="e2f68-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="e2f68-109">FALSE</span></span>  <br/> |<span data-ttu-id="e2f68-110">Não mostra a grade ao imprimir a página (o padrão).</span><span class="sxs-lookup"><span data-stu-id="e2f68-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2f68-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2f68-111">Remarks</span></span>

<span data-ttu-id="e2f68-p101">Esse valor corresponde à caixa de seleção **Linhas de grade** da guia **Configurar Impressão** da caixa de diálogo **Configurar Página** (na guia **Design**, clique na seta **Configurar Página**). Fora a cor (a versão impressa é cinza), a grade impressa é idêntica à grade que você vê na janela de desenho do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="e2f68-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="e2f68-114">Você pode escolher se deseja imprimir grade em uma base de página por página.</span><span class="sxs-lookup"><span data-stu-id="e2f68-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="e2f68-115">O estilo da grade também pode ser definido em uma base de página por página no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ) quando uma página estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="e2f68-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="e2f68-116">Para obter uma referência para a célula PrintGrid pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e2f68-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2f68-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e2f68-117">Cell name:</span></span>  <br/> |<span data-ttu-id="e2f68-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="e2f68-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="e2f68-119">Para obter uma referência para a célula PrintGrid pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e2f68-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2f68-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e2f68-120">Section index:</span></span>  <br/> |<span data-ttu-id="e2f68-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e2f68-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e2f68-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e2f68-122">Row index:</span></span>  <br/> |<span data-ttu-id="e2f68-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="e2f68-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="e2f68-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e2f68-124">Cell index:</span></span>  <br/> |<span data-ttu-id="e2f68-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="e2f68-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

