---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570909"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="3b1b7-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3b1b7-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="3b1b7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b1b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b1b7-105">Mantém e fornece acesso às propriedades de anexos em mensagens.</span><span class="sxs-lookup"><span data-stu-id="3b1b7-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="3b1b7-106">A interface **IAttach** não possui exclusivos métodos sua própria conta.</span><span class="sxs-lookup"><span data-stu-id="3b1b7-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="3b1b7-107">Para obter mais informações sobre como usar os anexos, consulte [As tabelas de anexo](attachment-tables.md)e [Anexos de MAPI](mapi-attachments.md) .</span><span class="sxs-lookup"><span data-stu-id="3b1b7-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b1b7-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3b1b7-108">Header file:</span></span>  <br/> |<span data-ttu-id="3b1b7-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b1b7-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3b1b7-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="3b1b7-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="3b1b7-111">Objetos de anexo</span><span class="sxs-lookup"><span data-stu-id="3b1b7-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="3b1b7-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="3b1b7-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="3b1b7-113">Provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="3b1b7-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="3b1b7-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="3b1b7-114">Called by:</span></span>  <br/> |<span data-ttu-id="3b1b7-115">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="3b1b7-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="3b1b7-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="3b1b7-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3b1b7-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="3b1b7-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="3b1b7-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="3b1b7-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="3b1b7-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="3b1b7-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="3b1b7-120">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="3b1b7-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="3b1b7-121">Transacionadas</span><span class="sxs-lookup"><span data-stu-id="3b1b7-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3b1b7-122">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="3b1b7-122">Vtable order</span></span>

<span data-ttu-id="3b1b7-123">Essa interface não tem quaisquer métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="3b1b7-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="3b1b7-124">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="3b1b7-124">**Required properties**</span></span>|<span data-ttu-id="3b1b7-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="3b1b7-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b1b7-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3b1b7-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3b1b7-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b1b7-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="3b1b7-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3b1b7-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3b1b7-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b1b7-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="3b1b7-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3b1b7-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3b1b7-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b1b7-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b1b7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b1b7-132">See also</span></span>



[<span data-ttu-id="3b1b7-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3b1b7-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

