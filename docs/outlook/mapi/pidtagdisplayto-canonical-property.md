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
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360785"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="a672d-103">Propriedade canônica PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="a672d-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="a672d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a672d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a672d-105">Contém uma lista de nomes de exibição dos destinatários de mensagens primárias (para), separados por ponto e vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="a672d-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a672d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a672d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a672d-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="a672d-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="a672d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a672d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a672d-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="a672d-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="a672d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a672d-110">Data type:</span></span>  <br/> |<span data-ttu-id="a672d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a672d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a672d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a672d-112">Area:</span></span>  <br/> |<span data-ttu-id="a672d-113">Mensagem</span><span class="sxs-lookup"><span data-stu-id="a672d-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a672d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a672d-114">Remarks</span></span>

<span data-ttu-id="a672d-115">O repositório de mensagens computa essas propriedades em objetos de mensagem usando o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="a672d-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="a672d-116">O repositório de mensagens também mantém essas propriedades para que ela sempre reflita o último estado salvo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a672d-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="a672d-117">O valor é sincronizado no momento de cada chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="a672d-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="a672d-118">Se uma mensagem não tiver destinatários primários, o repositório de mensagens deverá responder a uma chamada a [IMAPIProp::](imapiprop-getprops.md) GetProps com um valor de retorno de S_OK e uma cadeia de caracteres vazia para o **PR_DISPLAY_TO**.</span><span class="sxs-lookup"><span data-stu-id="a672d-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="a672d-119">Devido à possível necessidade de localização, a MAPI fornece essas diretrizes para todos os nomes de destinatários:</span><span class="sxs-lookup"><span data-stu-id="a672d-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="a672d-120">Todos os nomes devem ser capazes de ser localizados.</span><span class="sxs-lookup"><span data-stu-id="a672d-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="a672d-121">O ponto e vírgula deve ser o caractere usado para separar nomes nas propriedades **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e **PR_DISPLAY_TO** .</span><span class="sxs-lookup"><span data-stu-id="a672d-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="a672d-122">Pontos-e-vírgulas não são permitidos em nomes de destinatários no MAPI.</span><span class="sxs-lookup"><span data-stu-id="a672d-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="a672d-123">Os clientes devem traduzir cada ponto-e-vírgula encontrado no **PR_DISPLAY_TO** e as propriedades relacionadas para um caractere separador localizado antes de tornar as informações visíveis na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a672d-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="a672d-124">Ao encaminhar mensagens, os clientes não precisam traduzir os caracteres separadores na linha de destinatário principal.</span><span class="sxs-lookup"><span data-stu-id="a672d-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="a672d-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a672d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a672d-126">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="a672d-126">Protocol specifications</span></span>

<span data-ttu-id="a672d-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a672d-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a672d-128">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a672d-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a672d-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a672d-129">Header files</span></span>

<span data-ttu-id="a672d-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a672d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a672d-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a672d-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="a672d-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a672d-132">Mapitags.h</span></span>
  
> <span data-ttu-id="a672d-133">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a672d-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a672d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a672d-134">See also</span></span>



[<span data-ttu-id="a672d-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a672d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a672d-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a672d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a672d-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a672d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a672d-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a672d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

