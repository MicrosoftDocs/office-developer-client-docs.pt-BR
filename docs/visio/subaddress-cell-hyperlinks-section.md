---
title: Célula SubAddress (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Especifica uma localidade no documento de destino à qual vincular.
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773087"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="00a76-103">Célula SubAddress (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="00a76-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="00a76-104">Especifica uma localidade no documento de destino à qual vincular.</span><span class="sxs-lookup"><span data-stu-id="00a76-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00a76-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="00a76-105">Remarks</span></span>

<span data-ttu-id="00a76-106">Por exemplo, se a célula Address for "Drawing1.vsdx", a célula SubAddress pode especificar um nome de página como "Página-3".</span><span class="sxs-lookup"><span data-stu-id="00a76-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="00a76-107">Se a célula Address for o arquivo do Microsoft Excel "Samples.xlsx", o valor dessa célula pode ser uma planilha ou um intervalo em uma planilha, como "Funções de planilha" ou "Sheet1! A1: D10 ".</span><span class="sxs-lookup"><span data-stu-id="00a76-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="00a76-108">Se a célula Address for "http://www.microsoft.com/office/", o valor dessa célula pode ser uma âncora nomeada dentro do documento, como "soluções".</span><span class="sxs-lookup"><span data-stu-id="00a76-108">If the Address cell is "http://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="00a76-109">Você pode também definir o valor da célula utilizando a caixa de diálogo **Hiperlinks** (no grupo **Links** da guia **Inserir**, clique em **Hyperlink**).</span><span class="sxs-lookup"><span data-stu-id="00a76-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="00a76-110">Para obter uma referência para a célula SubAddress pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="00a76-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00a76-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="00a76-111">Cell name:</span></span>  <br/> | <span data-ttu-id="00a76-112">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="00a76-112">Hyperlink.</span></span>  <span data-ttu-id="00a76-113">*nome* . Subendereço onde Hyperlink *. nome* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="00a76-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="00a76-114">Para obter uma referência para a célula **SubAddress** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="00a76-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00a76-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="00a76-115">Section index:</span></span>  <br/> |<span data-ttu-id="00a76-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="00a76-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="00a76-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="00a76-117">Row index:</span></span>  <br/> |<span data-ttu-id="00a76-118">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="00a76-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="00a76-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="00a76-119">Cell index:</span></span>  <br/> |<span data-ttu-id="00a76-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="00a76-120">**visHLinkSubAddress**</span></span> <br/> |
   

