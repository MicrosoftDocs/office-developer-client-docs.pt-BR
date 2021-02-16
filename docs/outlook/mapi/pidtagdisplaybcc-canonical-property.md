---
title: Propriedade canônica PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360813"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="5b87b-103">Propriedade canônica PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="5b87b-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="5b87b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b87b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b87b-105">Contém uma lista ASCII dos nomes para exibição de quaisquer destinatários de mensagem com cópia carbono (Cc), separados por ponto-e-vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="5b87b-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b87b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5b87b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b87b-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="5b87b-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="5b87b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5b87b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b87b-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="5b87b-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="5b87b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5b87b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b87b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5b87b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5b87b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5b87b-112">Area:</span></span>  <br/> |<span data-ttu-id="5b87b-113">Mensagem</span><span class="sxs-lookup"><span data-stu-id="5b87b-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b87b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b87b-114">Remarks</span></span>

<span data-ttu-id="5b87b-115">O armazenamento de mensagens calcula essas propriedades em objetos de mensagem usando o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="5b87b-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="5b87b-116">O armazenamento de mensagens também mantém essas propriedades para que ela sempre reflita o último estado salvo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5b87b-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="5b87b-117">O valor é sincronizado no momento de cada chamada para o [método IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="5b87b-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="5b87b-118">Se uma mensagem não tiver destinatários com cópia carbono, o armazenamento de mensagens deverá responder a uma chamada [IMAPIProp::GetProps](imapiprop-getprops.md) com um valor de retorno de S_OK e uma cadeia de caracteres vazia para **PR_DISPLAY_BCC**.</span><span class="sxs-lookup"><span data-stu-id="5b87b-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="5b87b-119">Devido à possível necessidade de localização, o MAPI fornece estas diretrizes para todos os nomes de destinatários:</span><span class="sxs-lookup"><span data-stu-id="5b87b-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="5b87b-120">Todos os nomes devem ser localizados.</span><span class="sxs-lookup"><span data-stu-id="5b87b-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="5b87b-121">O ponto-e-vírgula deve ser o caractere usado para separar nomes nas propriedades **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5b87b-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="5b87b-122">Pontos-e-vírgulas não são permitidos em nomes de destinatários em MAPI.</span><span class="sxs-lookup"><span data-stu-id="5b87b-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="5b87b-123">Os clientes devem converter cada ponto-e-vírgula encontrado nessa propriedade em um caractere separador localizado antes de tornar as informações de propriedade visíveis na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5b87b-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="5b87b-124">Ao encaminhar mensagens, os clientes não precisam traduzir os caracteres separadores na linha do destinatário com cópia carbono.</span><span class="sxs-lookup"><span data-stu-id="5b87b-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="5b87b-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b87b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b87b-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5b87b-126">Protocol specifications</span></span>

<span data-ttu-id="5b87b-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b87b-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b87b-128">Descreve o formato das mensagens usadas para enviar informações relacionadas ao compartilhamento de pastas no cliente.</span><span class="sxs-lookup"><span data-stu-id="5b87b-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b87b-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="5b87b-129">Header files</span></span>

<span data-ttu-id="5b87b-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b87b-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b87b-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5b87b-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b87b-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b87b-132">Mapitags.h</span></span>
  
> <span data-ttu-id="5b87b-133">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5b87b-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b87b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b87b-134">See also</span></span>



[<span data-ttu-id="5b87b-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b87b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b87b-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5b87b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b87b-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b87b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b87b-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5b87b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

