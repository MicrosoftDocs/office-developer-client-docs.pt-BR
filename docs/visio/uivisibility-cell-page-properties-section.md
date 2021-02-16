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
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437326"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="3b0c3-103">Célula UIVisibility (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="3b0c3-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="3b0c3-104">Determina se o nome da página será exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="3b0c3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-105">**Value**</span></span>|<span data-ttu-id="3b0c3-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-106">**Description**</span></span>|<span data-ttu-id="3b0c3-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b0c3-108">0</span><span class="sxs-lookup"><span data-stu-id="3b0c3-108">0</span></span>  <br/> |<span data-ttu-id="3b0c3-109">Exibe o nome da página na interface do usuário (o padrão).</span><span class="sxs-lookup"><span data-stu-id="3b0c3-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="3b0c3-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="3b0c3-111">1 </span><span class="sxs-lookup"><span data-stu-id="3b0c3-111">1</span></span>  <br/> |<span data-ttu-id="3b0c3-112">Não exibe o nome da página na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="3b0c3-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b0c3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b0c3-114">Remarks</span></span>

<span data-ttu-id="3b0c3-115">A definição da célula UIVisibility como **visUIVHidden** impede que a página seja exibida em qualquer parte da interface do usuário em que a cadeia de caracteres contendo o nome da página apareça.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="3b0c3-116">Por exemplo, a página não seria listada como uma opção no **Gerenciador de Desenho** nem nas guias de página.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="3b0c3-117">No entanto, a página permanecerá acessível se você usar automação ou caminhos de interface do usuário que não incluam o nome da página, por exemplo, o **comando** Imprimir.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="3b0c3-118">Essa célula é destinada ao uso com páginas de documento, e não com páginas de sobreposição de marcação, cuja célula UIVisibility é definida como **visUIVHidden** por padrão e não deve ser mudada.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b0c3-119">Para ocultar uma página do  comando Imprimir do documento, torná-la uma página de plano de fundo ( a propriedade **Type** é **visTypeBackground** ) que não é usada como plano de fundo por qualquer página (as formas em páginas de plano de fundo são impressas quando uma página que a utiliza como plano de fundo é impressa).</span><span class="sxs-lookup"><span data-stu-id="3b0c3-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="3b0c3-120">O comando Imprimir **do** documento só funciona com páginas indexadas, e as páginas de plano de fundo não são indexadas.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="3b0c3-121">Para obter uma referência para a célula UIVisibility pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3b0c3-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b0c3-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3b0c3-122">Cell name:</span></span>  <br/> |<span data-ttu-id="3b0c3-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="3b0c3-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="3b0c3-124">Para obter uma referência para a célula UIVisibility pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3b0c3-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b0c3-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3b0c3-125">Section index:</span></span>  <br/> |<span data-ttu-id="3b0c3-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3b0c3-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3b0c3-127">Row index:</span></span>  <br/> |<span data-ttu-id="3b0c3-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="3b0c3-129">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="3b0c3-129">Cell index:</span></span>  <br/> |<span data-ttu-id="3b0c3-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="3b0c3-130">**visPageUIVisibility**</span></span> <br/> |
   

