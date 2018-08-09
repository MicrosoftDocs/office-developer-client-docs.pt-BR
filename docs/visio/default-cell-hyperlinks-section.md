---
title: Célula Default (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Determina o hiperlink padrão de uma forma ou página. Defina o valor desta célula para VERDADEIRO para atribuir um hiperlink como o padrão.
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771685"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="0fc0a-104">Célula Default (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="0fc0a-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="0fc0a-p102">Determina o hiperlink padrão de uma forma ou página. Defina o valor desta célula para VERDADEIRO para atribuir um hiperlink como o padrão.</span><span class="sxs-lookup"><span data-stu-id="0fc0a-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fc0a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fc0a-107">Remarks</span></span>

<span data-ttu-id="0fc0a-p103">Também é possível definir o hiperlink padrão selecionando uma forma, clicando em **Hiperlink**, na guia **Inserir**, selecionando um hiperlink e clicando em **Padrão**. O hiperlink padrão é exibido em negrito.</span><span class="sxs-lookup"><span data-stu-id="0fc0a-p103">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**. The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="0fc0a-110">Para obter uma referência para a célula Default pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0fc0a-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fc0a-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0fc0a-111">Cell name:</span></span>  <br/> |<span data-ttu-id="0fc0a-112">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="0fc0a-112">Hyperlink.</span></span> <span data-ttu-id="0fc0a-113">*Nome* . Padrão onde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="0fc0a-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="0fc0a-114">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="0fc0a-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="0fc0a-115">Para obter uma referência para a célula Default pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0fc0a-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fc0a-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0fc0a-116">Section index:</span></span>  <br/> |<span data-ttu-id="0fc0a-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="0fc0a-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="0fc0a-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0fc0a-118">Row index:</span></span>  <br/> |<span data-ttu-id="0fc0a-119">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0fc0a-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0fc0a-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0fc0a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0fc0a-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="0fc0a-121">**visHLinkDefault**</span></span> <br/> |
   

