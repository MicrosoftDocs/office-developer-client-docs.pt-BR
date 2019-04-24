---
title: Propriedade canônica PidTagOriginalSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEmailAddress
api_type:
- COM
ms.assetid: cc86505c-e264-435f-ae21-4a10f0bbf082
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ed3d84667d7be9c06d0ddf4d896b8888694edc12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355269"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="d9fbd-103">Propriedade canônica PidTagOriginalSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d9fbd-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="d9fbd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9fbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9fbd-105">Contém o endereço de email do remetente da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="d9fbd-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9fbd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d9fbd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9fbd-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="d9fbd-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="d9fbd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d9fbd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9fbd-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="d9fbd-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="d9fbd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d9fbd-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9fbd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9fbd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d9fbd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d9fbd-112">Area:</span></span>  <br/> |<span data-ttu-id="d9fbd-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="d9fbd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9fbd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9fbd-114">Remarks</span></span>

<span data-ttu-id="d9fbd-115">Essas propriedades são exemplos das propriedades de endereço para o remetente original de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d9fbd-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="d9fbd-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade com o valor de **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9fbd-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="d9fbd-117">Ela nunca é alterada quando a mensagem é encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="d9fbd-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d9fbd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9fbd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9fbd-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="d9fbd-119">Protocol specifications</span></span>

<span data-ttu-id="d9fbd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9fbd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9fbd-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d9fbd-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9fbd-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9fbd-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9fbd-123">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d9fbd-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9fbd-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d9fbd-124">Header files</span></span>

<span data-ttu-id="d9fbd-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d9fbd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9fbd-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d9fbd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9fbd-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d9fbd-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d9fbd-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d9fbd-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9fbd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9fbd-129">See also</span></span>



[<span data-ttu-id="d9fbd-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d9fbd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9fbd-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d9fbd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9fbd-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d9fbd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9fbd-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d9fbd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

