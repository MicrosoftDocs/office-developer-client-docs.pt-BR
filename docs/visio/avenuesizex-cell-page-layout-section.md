---
title: Célula AvenueSizeX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Determina a quantidade de espaço horizontal entre as formas na página de desenho quando você formate formas usando a caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Re-Layout Página e em Mais Opções de Layout).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411642"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="cec85-103">Célula AvenueSizeX (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="cec85-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="cec85-104">Determina a quantidade de espaço horizontal entre as formas na página de desenho quando você forma o layout de formas usando a caixa de diálogo Configurar **Layout** (na guia **Design,** no grupo **Layout,** clique em **Re-Layout Page** e em \*\* Mais Opções de Layout \*\*).</span><span class="sxs-lookup"><span data-stu-id="cec85-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click \*\* More Layout Options \*\*).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cec85-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="cec85-105">Remarks</span></span>

<span data-ttu-id="cec85-106">Também é possível definir esse valor na caixa de diálogo **Espaçamento de Layout e Direcionamento** (na guia **Design**, clique na seta do grupo **Configurar Página**, clique na guia **Layout e Direcionamento** e em **Espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="cec85-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="cec85-p101">A grade dinâmica utilizará a configuração na célula AvenueSizeX somente quando uma forma estiver disponível para o cálculo do espaçamento horizontal. Para utilizar a grade dinâmica, na guia **Exibir**, no grupo **Auxílios Visuais**, selecione **Grade Dinâmica**.</span><span class="sxs-lookup"><span data-stu-id="cec85-p101">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="cec85-109">Para fazer referência à célula AvenueSizeX pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cec85-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cec85-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cec85-110">Cell name:</span></span>  <br/> | <span data-ttu-id="cec85-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="cec85-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="cec85-112">Para obter uma referência para a célula AvenueSizeX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cec85-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cec85-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cec85-113">Section index:</span></span>  <br/> |<span data-ttu-id="cec85-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cec85-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cec85-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="cec85-115">Row index:</span></span>  <br/> |<span data-ttu-id="cec85-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="cec85-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="cec85-117">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="cec85-117">Cell index:</span></span>  <br/> |<span data-ttu-id="cec85-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="cec85-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

