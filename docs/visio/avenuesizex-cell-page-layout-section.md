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
description: Determina a quantidade de espaço horizontal entre as formas na página de desenho ao dispor formas usando a caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Novo Layout de página e, em seguida, clique em mais opções de Layout).
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771298"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="479bd-103">Célula AvenueSizeX (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="479bd-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="479bd-104">Determina a quantidade de espaço horizontal entre as formas na página de desenho ao dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design** , no grupo **Layout** , clique em **Novo Layout de página**e, em seguida, clique em * * mais Opções de layout * *).</span><span class="sxs-lookup"><span data-stu-id="479bd-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click ** More Layout Options **).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="479bd-105">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="479bd-105">Remarks</span></span>

<span data-ttu-id="479bd-106">Você também pode definir esse valor na caixa de diálogo **Layout e roteamento espaçamento** (na guia **Design** , clique na seta do grupo **Configurar página** , clique na guia **Layout e roteamento** e clique em **espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="479bd-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="479bd-107">A grade dinâmica usa a configuração na célula AvenueSizeX quando somente uma forma está disponível para o cálculo de espaçamento horizontal.</span><span class="sxs-lookup"><span data-stu-id="479bd-107">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing.</span></span> <span data-ttu-id="479bd-108">Para usar a grade dinâmica, na guia **Exibir** , no grupo **Auxílios visuais** , selecione **Grade dinâmica**.</span><span class="sxs-lookup"><span data-stu-id="479bd-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="479bd-109">Para obter uma referência à célula AvenueSizeX pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="479bd-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="479bd-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="479bd-110">Cell name:</span></span>  <br/> | <span data-ttu-id="479bd-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="479bd-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="479bd-112">Para obter uma referência à célula AvenueSizeX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="479bd-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="479bd-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="479bd-113">Section index:</span></span>  <br/> |<span data-ttu-id="479bd-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="479bd-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="479bd-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="479bd-115">Row index:</span></span>  <br/> |<span data-ttu-id="479bd-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="479bd-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="479bd-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="479bd-117">Cell index:</span></span>  <br/> |<span data-ttu-id="479bd-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="479bd-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

