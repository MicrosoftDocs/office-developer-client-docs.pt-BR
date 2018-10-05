---
title: Propriedade canônica PidTagReceivedByEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEmailAddress
api_type:
- COM
ms.assetid: 5f9ebe20-b037-422b-9991-69f85122a706
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cea63037f926cdd178b6036c82e87cbba48d7347
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401521"
---
# <a name="pidtagreceivedbyemailaddress-canonical-property"></a><span data-ttu-id="cb7b2-103">Propriedade canônica PidTagReceivedByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cb7b2-103">PidTagReceivedByEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="cb7b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb7b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb7b2-105">Contém o endereço de email para o usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-105">Contains the email address for the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb7b2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cb7b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb7b2-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="cb7b2-107">PR_RECEIVED_BY_EMAIL_ADDRESS, PR_RECEIVED_BY_EMAIL_ADDRESS_A, PR_RECEIVED_BY_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="cb7b2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb7b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb7b2-109">0x0076</span><span class="sxs-lookup"><span data-stu-id="cb7b2-109">0x0076</span></span>  <br/> |
|<span data-ttu-id="cb7b2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cb7b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb7b2-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cb7b2-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="cb7b2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cb7b2-112">Area:</span></span>  <br/> |<span data-ttu-id="cb7b2-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="cb7b2-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb7b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb7b2-114">Remarks</span></span>

<span data-ttu-id="cb7b2-115">Essas propriedades são exemplos das propriedades de endereço para o usuário de mensagens que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-115">These properties are examples of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="cb7b2-116">Devem ser definidas pelo provedor de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-116">They must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cb7b2-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb7b2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb7b2-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb7b2-118">Protocol specifications</span></span>

<span data-ttu-id="cb7b2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb7b2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb7b2-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb7b2-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb7b2-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb7b2-122">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="cb7b2-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb7b2-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb7b2-124">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="cb7b2-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb7b2-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb7b2-126">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="cb7b2-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb7b2-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb7b2-128">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="cb7b2-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb7b2-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb7b2-130">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-130">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="cb7b2-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb7b2-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb7b2-132">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb7b2-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cb7b2-133">Header files</span></span>

<span data-ttu-id="cb7b2-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb7b2-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb7b2-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb7b2-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cb7b2-136">Mapitags.h</span></span>
  
> <span data-ttu-id="cb7b2-137">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="cb7b2-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb7b2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb7b2-138">See also</span></span>



[<span data-ttu-id="cb7b2-139">Propriedade canônica PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cb7b2-139">PidTagEmailAddress Canonical Property</span></span>](pidtagemailaddress-canonical-property.md)


[<span data-ttu-id="cb7b2-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb7b2-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb7b2-141">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cb7b2-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb7b2-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cb7b2-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb7b2-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cb7b2-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

