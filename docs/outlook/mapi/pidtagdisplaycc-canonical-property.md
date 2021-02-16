---
title: Propriedade canônica PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360806"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="3a41c-103">Propriedade canônica PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="3a41c-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="3a41c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a41c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a41c-105">Contém uma lista ASCII dos nomes para exibição de quaisquer destinatários de mensagem com cópia carbono (CC), separados por ponto-e-vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="3a41c-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a41c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3a41c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3a41c-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="3a41c-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="3a41c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3a41c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3a41c-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="3a41c-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="3a41c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3a41c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3a41c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3a41c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3a41c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3a41c-112">Area:</span></span>  <br/> |<span data-ttu-id="3a41c-113">Mensagem</span><span class="sxs-lookup"><span data-stu-id="3a41c-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a41c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a41c-114">Remarks</span></span>

<span data-ttu-id="3a41c-115">O armazenamento de mensagens calcula essas propriedades em objetos de mensagem usando o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="3a41c-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="3a41c-116">O armazenamento de mensagens também mantém essas propriedades para que ela sempre reflita o último estado salvo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3a41c-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="3a41c-117">O valor é sincronizado no momento de cada chamada para [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="3a41c-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="3a41c-118">Se uma mensagem não tiver destinatários de cópia carbono, o armazenamento de mensagens deverá responder a uma chamada [IMAPIProp::GetProps](imapiprop-getprops.md) com um valor de retorno S_OK e uma cadeia de caracteres vazia para essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3a41c-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="3a41c-119">Devido à possível necessidade de localização, o MAPI fornece estas diretrizes para todos os nomes de destinatários:</span><span class="sxs-lookup"><span data-stu-id="3a41c-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="3a41c-120">Todos os nomes devem ser localizados.</span><span class="sxs-lookup"><span data-stu-id="3a41c-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="3a41c-121">O ponto-e-vírgula deve ser o caractere usado para separar nomes nas propriedades **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** e **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3a41c-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="3a41c-122">Pontos-e-vírgulas não são permitidos em nomes de destinatários em MAPI.</span><span class="sxs-lookup"><span data-stu-id="3a41c-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="3a41c-123">Os clientes devem converter cada ponto-e-vírgula encontrado nessa propriedade em um caractere separador localizado antes de tornar as informações de propriedade visíveis na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a41c-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="3a41c-124">Ao encaminhar mensagens, os clientes não precisam traduzir os caracteres separadores na linha do destinatário da cópia carbono.</span><span class="sxs-lookup"><span data-stu-id="3a41c-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="3a41c-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a41c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3a41c-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3a41c-126">Protocol specifications</span></span>

<span data-ttu-id="3a41c-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3a41c-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3a41c-128">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="3a41c-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3a41c-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3a41c-129">Header files</span></span>

<span data-ttu-id="3a41c-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a41c-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="3a41c-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3a41c-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="3a41c-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3a41c-132">Mapitags.h</span></span>
  
> <span data-ttu-id="3a41c-133">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3a41c-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a41c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a41c-134">See also</span></span>



[<span data-ttu-id="3a41c-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3a41c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3a41c-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3a41c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3a41c-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3a41c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3a41c-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3a41c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

