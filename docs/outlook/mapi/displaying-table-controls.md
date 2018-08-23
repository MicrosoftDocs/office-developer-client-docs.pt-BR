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
ms.openlocfilehash: 7af1e710006986807091c5c36d54da86204a71d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568459"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="49e63-103">Exibir controles de tabela</span><span class="sxs-lookup"><span data-stu-id="49e63-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="49e63-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49e63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49e63-105">Há muitos tipos diferentes de controles, nenhum exclusivas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="49e63-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="49e63-106">No entanto, MAPI define suas próprias estruturas usadas em conjunto com [BuildDisplayTable](builddisplaytable.md) para descrever o conjunto exclusivo de dados envolvidos com cada controle.</span><span class="sxs-lookup"><span data-stu-id="49e63-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="49e63-107">A tabela a seguir lista as estruturas que descrevem cada tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="49e63-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="49e63-108">**Estrutura de controle**</span><span class="sxs-lookup"><span data-stu-id="49e63-108">**Control structure**</span></span>|<span data-ttu-id="49e63-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="49e63-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49e63-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="49e63-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="49e63-111">Descreve um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="49e63-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="49e63-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="49e63-113">Descreve um controle de caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="49e63-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="49e63-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="49e63-115">Descreve um controle de caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="49e63-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="49e63-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="49e63-117">Descreve um controle de caixa de listagem suspensa.</span><span class="sxs-lookup"><span data-stu-id="49e63-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="49e63-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="49e63-119">Descreve um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="49e63-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="49e63-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="49e63-121">Descreve um controle de caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="49e63-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="49e63-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="49e63-123">Descreve um controle label.</span><span class="sxs-lookup"><span data-stu-id="49e63-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="49e63-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="49e63-125">Descreve um controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="49e63-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="49e63-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="49e63-127">Descreve um controle de caixa de listagem suspensa de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="49e63-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="49e63-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="49e63-129">Descreve um controle de caixa de listagem de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="49e63-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="49e63-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="49e63-131">Descreve um controle de páginas com guias.</span><span class="sxs-lookup"><span data-stu-id="49e63-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="49e63-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="49e63-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="49e63-133">Descreve um controle de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="49e63-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49e63-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="49e63-134">See also</span></span>



[<span data-ttu-id="49e63-135">Implementação da tabela de exibição</span><span class="sxs-lookup"><span data-stu-id="49e63-135">Display Table Implementation</span></span>](display-table-implementation.md)

