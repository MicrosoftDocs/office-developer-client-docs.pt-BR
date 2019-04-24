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
ms.openlocfilehash: 37f6cd0320894d500416672c3dd0d90ee3324b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337027"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="278b2-103">Exibir controles de tabela</span><span class="sxs-lookup"><span data-stu-id="278b2-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="278b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="278b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="278b2-105">Há muitos tipos diferentes de controles, nenhum exclusivo para MAPI.</span><span class="sxs-lookup"><span data-stu-id="278b2-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="278b2-106">No enTanto, o MAPI define suas próprias estruturas que são usadas em conjunto com o [BuildDisplayTable](builddisplaytable.md) para descrever o conjunto exclusivo de dados envolvidos em cada controle.</span><span class="sxs-lookup"><span data-stu-id="278b2-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="278b2-107">A tabela a seguir lista as estruturas que descrevem cada tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="278b2-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="278b2-108">**Estrutura de controle**</span><span class="sxs-lookup"><span data-stu-id="278b2-108">**Control structure**</span></span>|<span data-ttu-id="278b2-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="278b2-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="278b2-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="278b2-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="278b2-111">Descreve um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="278b2-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="278b2-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="278b2-113">Descreve um controle de caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="278b2-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="278b2-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="278b2-115">Descreve um controle de caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="278b2-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="278b2-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="278b2-117">Descreve um controle de caixa de listagem suspensa.</span><span class="sxs-lookup"><span data-stu-id="278b2-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="278b2-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="278b2-119">Descreve um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="278b2-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="278b2-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="278b2-121">Descreve um controle de caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="278b2-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="278b2-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="278b2-123">Descreve um controle Label.</span><span class="sxs-lookup"><span data-stu-id="278b2-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="278b2-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="278b2-125">Descreve um controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="278b2-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="278b2-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="278b2-127">Descreve um controle de caixa de listagem suspensa de vários valores.</span><span class="sxs-lookup"><span data-stu-id="278b2-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="278b2-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="278b2-129">Descreve um controle de caixa de listagem de vários valores.</span><span class="sxs-lookup"><span data-stu-id="278b2-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="278b2-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="278b2-131">Descreve um controle de página com guias.</span><span class="sxs-lookup"><span data-stu-id="278b2-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="278b2-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="278b2-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="278b2-133">Descreve um controle de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="278b2-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="278b2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="278b2-134">See also</span></span>



[<span data-ttu-id="278b2-135">Exibir a implementação da tabela</span><span class="sxs-lookup"><span data-stu-id="278b2-135">Display Table Implementation</span></span>](display-table-implementation.md)

