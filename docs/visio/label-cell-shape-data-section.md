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
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420175"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="9e1a7-104">Célula Label (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="9e1a7-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="9e1a7-105">Especifica o rótulo exibido aos usuários na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="9e1a7-106">Um rótulo consiste em caracteres alfanuméricos, incluindo o caractere de sublinhado (_).</span><span class="sxs-lookup"><span data-stu-id="9e1a7-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9e1a7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e1a7-107">Remarks</span></span>

<span data-ttu-id="9e1a7-108">O aplicativo inclui automaticamente a cadeia de caracteres do rótulo entre aspas na célula, embora as aspas não sejam exibidas na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="9e1a7-109">Se nenhum texto para o rótulo for localizado, o Visio exibirá o nome da linha (Prop.Linha) na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="9e1a7-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="9e1a7-110">Para obter uma referência para a célula Label pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9e1a7-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e1a7-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9e1a7-111">Cell name:</span></span>  <br/> |<span data-ttu-id="9e1a7-112">Prop. *Nome*  . Rotule onde Prop.  *Nome*  é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="9e1a7-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="9e1a7-113">Para obter uma referência para a célula Label pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9e1a7-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e1a7-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9e1a7-114">Section index:</span></span>  <br/> |<span data-ttu-id="9e1a7-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="9e1a7-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="9e1a7-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="9e1a7-116">Row index:</span></span>  <br/> |<span data-ttu-id="9e1a7-117">**visRowProp**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9e1a7-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9e1a7-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="9e1a7-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9e1a7-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="9e1a7-119">**visCustPropsLabel**</span></span> <br/> |
   

