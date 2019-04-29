---
title: Célula AvenueSizeY (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Determina a quantidade de espaço vertical entre as formas na página de desenho ao dispor as formas usando a caixa de diálogo Configurar layout (na guia Design, no grupo layout, clique em reFazer o layout da página e, em seguida, clique em mais opções de layout).
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420203"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="fa056-103">Célula AvenueSizeY (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="fa056-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="fa056-104">Determina a quantidade de espaço vertical entre as formas na página de desenho ao dispor as formas usando a caixa de diálogo **Configurar layout** (na guia **design** , no grupo **layout** , clique em refazer o **layout** da página e clique em **mais Opções de layout**).</span><span class="sxs-lookup"><span data-stu-id="fa056-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa056-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa056-105">Remarks</span></span>

<span data-ttu-id="fa056-106">Também é possível definir esse valor na caixa de diálogo **Espaçamento de Layout e Direcionamento** (na guia **Design**, clique na seta do grupo **Configurar Página**, clique na guia **Layout e Direcionamento** e em **Espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="fa056-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="fa056-p101">A grade dinâmica utilizará a configuração na célula AvenueSizeY somente quando uma forma estiver disponível para o cálculo do espaçamento vertical. Para utilizar a grade dinâmica, na guia **Exibir**, no grupo **Auxílios Visuais**, selecione **Grade Dinâmica**.</span><span class="sxs-lookup"><span data-stu-id="fa056-p101">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="fa056-109">Para obter uma referência para a célula AvenueSizeY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="fa056-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa056-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fa056-110">Cell name:</span></span>  <br/> | <span data-ttu-id="fa056-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="fa056-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="fa056-112">Para obter uma referência para a célula AvenueSizeY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fa056-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa056-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fa056-113">Section index:</span></span>  <br/> |<span data-ttu-id="fa056-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fa056-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fa056-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="fa056-115">Row index:</span></span>  <br/> |<span data-ttu-id="fa056-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="fa056-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="fa056-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="fa056-117">Cell index:</span></span>  <br/> |<span data-ttu-id="fa056-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="fa056-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

