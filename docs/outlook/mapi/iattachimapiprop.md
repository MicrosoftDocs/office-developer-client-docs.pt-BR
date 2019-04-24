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
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341619"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="fcbfe-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fcbfe-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="fcbfe-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcbfe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcbfe-105">Mantém e fornece acesso às propriedades de anexos em mensagens.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="fcbfe-106">A interface **IAttach** não tem métodos exclusivos próprios.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="fcbfe-107">Para obter mais informações sobre como usar anexos, consulte [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fcbfe-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcbfe-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fcbfe-108">Header file:</span></span>  <br/> |<span data-ttu-id="fcbfe-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fcbfe-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fcbfe-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="fcbfe-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="fcbfe-111">Objetos Attachment</span><span class="sxs-lookup"><span data-stu-id="fcbfe-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="fcbfe-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="fcbfe-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="fcbfe-113">Provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="fcbfe-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="fcbfe-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="fcbfe-114">Called by:</span></span>  <br/> |<span data-ttu-id="fcbfe-115">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="fcbfe-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="fcbfe-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="fcbfe-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fcbfe-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="fcbfe-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="fcbfe-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="fcbfe-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="fcbfe-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="fcbfe-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="fcbfe-120">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="fcbfe-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="fcbfe-121">Transact</span><span class="sxs-lookup"><span data-stu-id="fcbfe-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fcbfe-122">Vtable order</span><span class="sxs-lookup"><span data-stu-id="fcbfe-122">Vtable order</span></span>

<span data-ttu-id="fcbfe-123">Esta interface não tem nenhum método exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="fcbfe-124">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="fcbfe-124">**Required properties**</span></span>|<span data-ttu-id="fcbfe-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="fcbfe-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcbfe-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fcbfe-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fcbfe-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcbfe-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="fcbfe-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fcbfe-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fcbfe-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcbfe-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="fcbfe-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fcbfe-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fcbfe-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcbfe-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcbfe-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcbfe-132">See also</span></span>



[<span data-ttu-id="fcbfe-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="fcbfe-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

