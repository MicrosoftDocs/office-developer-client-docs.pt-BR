---
title: Propriedade canônica PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 79a0307aaf8b91a50485234acc2e1cbdd2314b47
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574164"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="9edda-103">Propriedade canônica PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="9edda-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="9edda-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9edda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9edda-105">Contém uma lista dos nomes de exibição de primário (para) destinatários da mensagem, separados por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="9edda-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9edda-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9edda-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9edda-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="9edda-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="9edda-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9edda-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9edda-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="9edda-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="9edda-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9edda-110">Data type:</span></span>  <br/> |<span data-ttu-id="9edda-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9edda-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9edda-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9edda-112">Area:</span></span>  <br/> |<span data-ttu-id="9edda-113">Message</span><span class="sxs-lookup"><span data-stu-id="9edda-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9edda-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9edda-114">Remarks</span></span>

<span data-ttu-id="9edda-115">O armazenamento de mensagens computa essas propriedades em objetos de mensagem usando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="9edda-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="9edda-116">O armazenamento de mensagens também mantém essas propriedades para que ela sempre reflete o último estado salvo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9edda-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="9edda-117">O valor é sincronizado no momento de cada chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="9edda-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="9edda-118">Se uma mensagem não tiver principais destinatários, o armazenamento de mensagens deve responder a uma chamada [IMAPIProp::GetProps](imapiprop-getprops.md) com um valor de retorno de S_OK e uma sequência vazia para **PR_DISPLAY_TO**.</span><span class="sxs-lookup"><span data-stu-id="9edda-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="9edda-119">Devido a necessidade de possível de localização, MAPI fornece estas diretrizes para todos os nomes de destinatário:</span><span class="sxs-lookup"><span data-stu-id="9edda-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="9edda-120">Todos os nomes devem ser capazes de ser localizadas.</span><span class="sxs-lookup"><span data-stu-id="9edda-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="9edda-121">O ponto e vírgula deve ser o caractere usado para separar nomes nas propriedades **PR_DISPLAY_TO** , **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9edda-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="9edda-122">Ponto e vírgula não é permitida em nomes de destinatários em MAPI.</span><span class="sxs-lookup"><span data-stu-id="9edda-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="9edda-123">Clientes devem traduzir cada ponto e vírgula encontrada no **PR_DISPLAY_TO** e propriedades relacionadas a um caractere separador localizado antes de fazer as informações visível na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9edda-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="9edda-124">Quando o encaminhamento de mensagens, os clientes não precisará convertem os caracteres separadores na linha de destinatário principal.</span><span class="sxs-lookup"><span data-stu-id="9edda-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="9edda-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9edda-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9edda-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9edda-126">Protocol specifications</span></span>

<span data-ttu-id="9edda-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9edda-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9edda-128">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9edda-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9edda-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9edda-129">Header files</span></span>

<span data-ttu-id="9edda-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9edda-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="9edda-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9edda-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="9edda-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9edda-132">Mapitags.h</span></span>
  
> <span data-ttu-id="9edda-133">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9edda-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9edda-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9edda-134">See also</span></span>



[<span data-ttu-id="9edda-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9edda-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9edda-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9edda-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9edda-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9edda-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9edda-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9edda-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

