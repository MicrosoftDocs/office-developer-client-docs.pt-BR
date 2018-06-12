---
title: Célula UIVisibility (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Determina se o nome da página será exibido na interface do usuário.
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773234"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="c1907-103">Célula UIVisibility (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="c1907-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="c1907-104">Determina se o nome da página será exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1907-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="c1907-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c1907-105">**Value**</span></span>|<span data-ttu-id="c1907-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c1907-106">**Description**</span></span>|<span data-ttu-id="c1907-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="c1907-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1907-108">0</span><span class="sxs-lookup"><span data-stu-id="c1907-108">0</span></span>  <br/> |<span data-ttu-id="c1907-109">Exibe o nome da página na interface do usuário (o padrão).</span><span class="sxs-lookup"><span data-stu-id="c1907-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="c1907-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="c1907-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="c1907-111">1</span><span class="sxs-lookup"><span data-stu-id="c1907-111">1</span></span>  <br/> |<span data-ttu-id="c1907-112">Não exibe o nome da página na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1907-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="c1907-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="c1907-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1907-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c1907-114">Remarks</span></span>

<span data-ttu-id="c1907-115">Definindo a célula UIVisibility como **visUIVHidden** impede que a página que aparecem em qualquer lugar na interface de usuário onde a cadeia de caracteres contendo o nome da página aparece.</span><span class="sxs-lookup"><span data-stu-id="c1907-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="c1907-116">Por exemplo, a página não seria listada como uma opção no **Gerenciador de desenho** ou nas guias de página.</span><span class="sxs-lookup"><span data-stu-id="c1907-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="c1907-117">A página permanece acessível, no entanto, se você usar caminhos de automação ou da interface do usuário que não inclua o nome da página, por exemplo, o comando **Imprimir** .</span><span class="sxs-lookup"><span data-stu-id="c1907-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="c1907-118">Esta célula é destinada para uso com páginas do documento; ele não é destinado para uso com páginas de sobreposição de marcação, que possuem a célula UIVisibility definida como **visUIVHidden** por padrão e não deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="c1907-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c1907-119">Para ocultar uma página do comando **Imprimir** do documento, torná-lo uma página de plano de fundo (a propriedade**Type** é **visTypeBackground** ) que não é usado como um plano de fundo por qualquer página (as formas em páginas são impressas quando uma página utilizá-lo como um plano de fundo é de plano de fundo impresso).</span><span class="sxs-lookup"><span data-stu-id="c1907-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="c1907-120">Comando **Imprimir** do documento funciona somente com páginas indexadas e páginas de plano de fundo não estão indexadas.</span><span class="sxs-lookup"><span data-stu-id="c1907-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="c1907-121">Para obter uma referência para a célula UIVisibility pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c1907-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1907-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c1907-122">Cell name:</span></span>  <br/> |<span data-ttu-id="c1907-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="c1907-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="c1907-124">Para obter uma referência para a célula UIVisibility pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c1907-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1907-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c1907-125">Section index:</span></span>  <br/> |<span data-ttu-id="c1907-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c1907-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c1907-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c1907-127">Row index:</span></span>  <br/> |<span data-ttu-id="c1907-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="c1907-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="c1907-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c1907-129">Cell index:</span></span>  <br/> |<span data-ttu-id="c1907-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="c1907-130">**visPageUIVisibility**</span></span> <br/> |
   

