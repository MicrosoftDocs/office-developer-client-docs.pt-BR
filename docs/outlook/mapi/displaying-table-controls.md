---
title: Exibir controles de tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 11b3279582c4cfb0d2c2249c6f4eddd7f0260b49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766440"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="52293-103">Exibir controles de tabela</span><span class="sxs-lookup"><span data-stu-id="52293-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="52293-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52293-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52293-105">Há muitos tipos diferentes de controles, nenhum exclusivas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="52293-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="52293-106">No entanto, MAPI define suas próprias estruturas usadas em conjunto com [BuildDisplayTable](builddisplaytable.md) para descrever o conjunto exclusivo de dados envolvidos com cada controle.</span><span class="sxs-lookup"><span data-stu-id="52293-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="52293-107">A tabela a seguir lista as estruturas que descrevem cada tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="52293-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="52293-108">**Estrutura de controle**</span><span class="sxs-lookup"><span data-stu-id="52293-108">**Control structure**</span></span>|<span data-ttu-id="52293-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52293-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52293-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="52293-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="52293-111">Descreve um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="52293-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="52293-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="52293-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="52293-113">Descreve um controle de caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="52293-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="52293-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="52293-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="52293-115">Descreve um controle de caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="52293-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="52293-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="52293-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="52293-117">Descreve um controle de caixa de listagem suspensa.</span><span class="sxs-lookup"><span data-stu-id="52293-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="52293-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="52293-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="52293-119">Descreve um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="52293-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="52293-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="52293-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="52293-121">Descreve um controle de caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="52293-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="52293-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="52293-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="52293-123">Descreve um controle label.</span><span class="sxs-lookup"><span data-stu-id="52293-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="52293-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="52293-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="52293-125">Descreve um controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="52293-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="52293-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="52293-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="52293-127">Descreve um controle de caixa de listagem suspensa de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="52293-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="52293-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="52293-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="52293-129">Descreve um controle de caixa de listagem de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="52293-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="52293-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="52293-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="52293-131">Descreve um controle de páginas com guias.</span><span class="sxs-lookup"><span data-stu-id="52293-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="52293-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="52293-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="52293-133">Descreve um controle de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="52293-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52293-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="52293-134">See also</span></span>



[<span data-ttu-id="52293-135">Implementação da tabela de exibição</span><span class="sxs-lookup"><span data-stu-id="52293-135">Display Table Implementation</span></span>](display-table-implementation.md)

