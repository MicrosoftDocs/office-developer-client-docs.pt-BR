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
description: Determina a quantidade de espaço vertical entre as formas na página de desenho ao dispor formas usando a caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Novo Layout de página e, em seguida, clique em mais opções de Layout).
ms.openlocfilehash: af4089a3b215efaf49b8a45929ca94799fffcba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771291"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="97d8b-103">Célula AvenueSizeY (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="97d8b-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="97d8b-104">Determina a quantidade de espaço vertical entre as formas na página de desenho ao dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design** , no grupo **Layout** , clique em **Novo Layout** de página e, em seguida, clique em **mais Opções de layout**).</span><span class="sxs-lookup"><span data-stu-id="97d8b-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97d8b-105">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="97d8b-105">Remarks</span></span>

<span data-ttu-id="97d8b-106">Você também pode definir esse valor na caixa de diálogo **Layout e roteamento espaçamento** (na guia **Design** , clique na seta do grupo **Configurar página** , clique na guia **Layout e roteamento** e clique em **espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="97d8b-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="97d8b-107">A grade dinâmica usa a configuração na célula AvenueSizeY quando somente uma forma está disponível para o cálculo de espaçamento vertical.</span><span class="sxs-lookup"><span data-stu-id="97d8b-107">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing.</span></span> <span data-ttu-id="97d8b-108">Para usar a grade dinâmica, na guia **Exibir** , no grupo **Auxílios visuais** , selecione **Grade dinâmica**.</span><span class="sxs-lookup"><span data-stu-id="97d8b-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="97d8b-109">Para obter uma referência para a célula AvenueSizeY pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="97d8b-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97d8b-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="97d8b-110">Cell name:</span></span>  <br/> | <span data-ttu-id="97d8b-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="97d8b-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="97d8b-112">Para obter uma referência para a célula AvenueSizeY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="97d8b-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97d8b-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="97d8b-113">Section index:</span></span>  <br/> |<span data-ttu-id="97d8b-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97d8b-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="97d8b-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="97d8b-115">Row index:</span></span>  <br/> |<span data-ttu-id="97d8b-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="97d8b-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="97d8b-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="97d8b-117">Cell index:</span></span>  <br/> |<span data-ttu-id="97d8b-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="97d8b-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

