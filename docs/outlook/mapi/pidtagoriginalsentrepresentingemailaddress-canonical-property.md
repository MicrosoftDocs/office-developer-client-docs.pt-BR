---
title: Propriedade canônica PidTagOriginalSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e2c3d2c3-5451-45cb-b0ec-bdbf5b39a0ba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2530e27993163505b28fa7d08fd5caf4cc9b03be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385351"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="d1052-103">Propriedade canônica PidTagOriginalSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d1052-103">PidTagOriginalSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="d1052-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1052-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1052-105">Contém o endereço de email do usuário mensagens em nome do qual a mensagem original foi enviada.</span><span class="sxs-lookup"><span data-stu-id="d1052-105">Contains the email address of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1052-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d1052-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1052-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="d1052-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="d1052-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d1052-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1052-109">0x0069</span><span class="sxs-lookup"><span data-stu-id="d1052-109">0x0069</span></span>  <br/> |
|<span data-ttu-id="d1052-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d1052-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1052-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1052-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d1052-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d1052-112">Area:</span></span>  <br/> |<span data-ttu-id="d1052-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="d1052-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1052-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1052-114">Remarks</span></span>

<span data-ttu-id="d1052-115">Essas propriedades são exemplos das propriedades de endereço de remetente de uma mensagem original representado.</span><span class="sxs-lookup"><span data-stu-id="d1052-115">These properties are examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="d1052-116">Ele é usado em um segmento de conversação.</span><span class="sxs-lookup"><span data-stu-id="d1052-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="d1052-117">Um aplicativo cliente enviar uma mensagem em nome de outro cliente deve definir essas propriedades com o valor da propriedade **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) no primeiro envio da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d1052-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="d1052-118">Depois de definido, ela nunca deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="d1052-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1052-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1052-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1052-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d1052-120">Protocol specifications</span></span>

<span data-ttu-id="d1052-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1052-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1052-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d1052-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1052-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1052-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1052-124">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d1052-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1052-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1052-125">Header files</span></span>

<span data-ttu-id="d1052-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1052-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1052-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d1052-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1052-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d1052-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d1052-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d1052-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1052-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1052-130">See also</span></span>



[<span data-ttu-id="d1052-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1052-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1052-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d1052-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1052-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d1052-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1052-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d1052-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

