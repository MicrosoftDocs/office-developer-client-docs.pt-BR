---
title: Célula Label (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Especifica o rótulo exibido aos usuários na janela Dados da Forma. Um rótulo consiste em caracteres alfanuméricos, incluindo o caractere de sublinhado (_).
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772126"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="6a93e-104">Célula Label (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="6a93e-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="6a93e-p102">Especifica o rótulo exibido aos usuários na janela **Dados da Forma**. Um rótulo consiste em caracteres alfanuméricos, incluindo o caractere de sublinhado (_).</span><span class="sxs-lookup"><span data-stu-id="6a93e-p102">Specifies the label that appears to users in the **Shape Data** window. A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a93e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a93e-107">Remarks</span></span>

<span data-ttu-id="6a93e-108">O aplicativo inclui automaticamente a cadeia de caracteres do rótulo entre aspas na célula, embora as aspas não sejam exibidas na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="6a93e-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="6a93e-109">Se nenhum texto para o rótulo for localizado, o Visio exibirá o nome da linha (Prop.Linha) na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="6a93e-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="6a93e-110">Para obter uma referência para a célula Label pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6a93e-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a93e-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6a93e-111">Cell name:</span></span>  <br/> |<span data-ttu-id="6a93e-112">Prop. *Nome* . Rótulo onde Prop.  *Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="6a93e-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6a93e-113">Para obter uma referência para a célula Label pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6a93e-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a93e-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6a93e-114">Section index:</span></span>  <br/> |<span data-ttu-id="6a93e-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6a93e-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="6a93e-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6a93e-116">Row index:</span></span>  <br/> |<span data-ttu-id="6a93e-117">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6a93e-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6a93e-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6a93e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6a93e-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="6a93e-119">**visCustPropsLabel**</span></span> <br/> |
   

