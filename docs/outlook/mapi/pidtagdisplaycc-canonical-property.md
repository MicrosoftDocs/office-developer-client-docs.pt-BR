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
ms.openlocfilehash: 3d27ad5fbc02e3883d6f74129323165394c4cf2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577727"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="a9f69-103">Propriedade canônica PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="a9f69-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="a9f69-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9f69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9f69-105">Contém uma lista de ASCII dos nomes de exibição de qualquer destinatários de cópia carbono (CC) da mensagem, separados por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="a9f69-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9f69-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a9f69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9f69-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="a9f69-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="a9f69-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a9f69-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9f69-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="a9f69-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="a9f69-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a9f69-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9f69-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a9f69-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a9f69-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a9f69-112">Area:</span></span>  <br/> |<span data-ttu-id="a9f69-113">Message</span><span class="sxs-lookup"><span data-stu-id="a9f69-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9f69-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9f69-114">Remarks</span></span>

<span data-ttu-id="a9f69-115">O armazenamento de mensagens computa essas propriedades em objetos de mensagem usando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f69-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="a9f69-116">O armazenamento de mensagens também mantém essas propriedades para que ela sempre reflete o último estado salvo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a9f69-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="a9f69-117">O valor é sincronizado no momento de cada chamada para [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="a9f69-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="a9f69-118">Se uma mensagem não tiver cópia carbono destinatários, o armazenamento de mensagens deve responder a uma chamada [IMAPIProp::GetProps](imapiprop-getprops.md) com um valor de retorno de S_OK e uma sequência vazia para essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a9f69-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="a9f69-119">Devido a necessidade de possível de localização, MAPI fornece estas diretrizes para todos os nomes de destinatário:</span><span class="sxs-lookup"><span data-stu-id="a9f69-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="a9f69-120">Todos os nomes devem ser capazes de ser localizadas.</span><span class="sxs-lookup"><span data-stu-id="a9f69-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="a9f69-121">O ponto e vírgula deve ser o caractere usado para separar nomes na **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**e propriedades de **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a9f69-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="a9f69-122">Ponto e vírgula não é permitida em nomes de destinatários em MAPI.</span><span class="sxs-lookup"><span data-stu-id="a9f69-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="a9f69-123">Os clientes devem traduzir cada ponto e vírgula encontrada nesta propriedade como um caractere separador localizado antes de fazer as informações de propriedade visível na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a9f69-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="a9f69-124">Quando o encaminhamento de mensagens, os clientes não precisará traduzir os caracteres separadores na linha de destinatário de cópia carbono.</span><span class="sxs-lookup"><span data-stu-id="a9f69-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="a9f69-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9f69-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9f69-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a9f69-126">Protocol specifications</span></span>

<span data-ttu-id="a9f69-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9f69-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9f69-128">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a9f69-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9f69-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a9f69-129">Header files</span></span>

<span data-ttu-id="a9f69-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9f69-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9f69-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a9f69-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9f69-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9f69-132">Mapitags.h</span></span>
  
> <span data-ttu-id="a9f69-133">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a9f69-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9f69-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9f69-134">See also</span></span>



[<span data-ttu-id="a9f69-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a9f69-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9f69-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a9f69-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9f69-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a9f69-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9f69-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a9f69-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

