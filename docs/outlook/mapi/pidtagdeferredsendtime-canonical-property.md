---
title: Propriedade canônica PidTagDeferredSendTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2d6374c2fd3c277e2bb976930e9e105cc839b1e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359875"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="a0edb-103">Propriedade canônica PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="a0edb-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="a0edb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0edb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0edb-105">Indica uma hora em que um cliente gostaria de adiar o envio de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a0edb-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0edb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a0edb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0edb-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="a0edb-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="a0edb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a0edb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0edb-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="a0edb-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="a0edb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a0edb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0edb-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a0edb-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a0edb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a0edb-112">Area:</span></span>  <br/> |<span data-ttu-id="a0edb-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="a0edb-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0edb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0edb-114">Remarks</span></span>

<span data-ttu-id="a0edb-115">Se as propriedades **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) e **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) estiverem presentes, o valor dessa propriedade será recalculado usando a fórmula a seguir e o valor antigo é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a0edb-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="a0edb-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="a0edb-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="a0edb-117">Se o valor **PR_DEFERRED_SEND_TIME** for anterior à hora atual (em UTC), a mensagem será enviada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a0edb-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a0edb-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0edb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0edb-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="a0edb-119">Protocol specifications</span></span>

<span data-ttu-id="a0edb-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0edb-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0edb-121">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a0edb-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0edb-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0edb-122">Header files</span></span>

<span data-ttu-id="a0edb-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a0edb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0edb-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a0edb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0edb-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a0edb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a0edb-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a0edb-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0edb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0edb-127">See also</span></span>



[<span data-ttu-id="a0edb-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a0edb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0edb-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a0edb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0edb-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a0edb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0edb-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a0edb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

