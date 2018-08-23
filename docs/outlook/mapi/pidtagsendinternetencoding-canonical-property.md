---
title: Propriedade canônica PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 33b9931a269eb4b5ee0429287d60fa1962b0e4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584230"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="05eab-103">Propriedade canônica PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="05eab-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="05eab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05eab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05eab-105">Contém uma bitmask dos preferências de codificação.</span><span class="sxs-lookup"><span data-stu-id="05eab-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05eab-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="05eab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05eab-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="05eab-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="05eab-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="05eab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05eab-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="05eab-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="05eab-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="05eab-110">Data type:</span></span>  <br/> |<span data-ttu-id="05eab-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="05eab-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="05eab-112">Área:</span><span class="sxs-lookup"><span data-stu-id="05eab-112">Area:</span></span>  <br/> |<span data-ttu-id="05eab-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="05eab-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05eab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="05eab-114">Remarks</span></span>

<span data-ttu-id="05eab-115">Defina essa propriedade para indicar as opções de codificação usadas.</span><span class="sxs-lookup"><span data-stu-id="05eab-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="05eab-116">Essa propriedade contém os sinalizadores a seguir:</span><span class="sxs-lookup"><span data-stu-id="05eab-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="05eab-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="05eab-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="05eab-118">Codifica o texto da mensagem em HTML.</span><span class="sxs-lookup"><span data-stu-id="05eab-118">Encode the message text in HTML.</span></span> <span data-ttu-id="05eab-119">Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido.</span><span class="sxs-lookup"><span data-stu-id="05eab-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="05eab-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="05eab-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="05eab-121">Codifica o texto da mensagem usando texto e HTML como alternativas de várias partes do Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="05eab-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="05eab-122">Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido.</span><span class="sxs-lookup"><span data-stu-id="05eab-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="05eab-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="05eab-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="05eab-124">Codifica a mensagem usando MIME.</span><span class="sxs-lookup"><span data-stu-id="05eab-124">Encode the message using MIME.</span></span> <span data-ttu-id="05eab-125">Se esse sinalizador não estiver definida, o MAPI codifica o texto da mensagem em texto sem formatação e os anexos em UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="05eab-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="05eab-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="05eab-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="05eab-127">Use os outros sinalizadores neste bitmask para determinar a codificação.</span><span class="sxs-lookup"><span data-stu-id="05eab-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="05eab-128">Se esse sinalizador não estiver definida, MAPI deixa para o sistema de mensagens para tomar decisões de codificação.</span><span class="sxs-lookup"><span data-stu-id="05eab-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="05eab-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="05eab-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="05eab-130">Codifica anexos do Macintosh no modo duplo da Apple.</span><span class="sxs-lookup"><span data-stu-id="05eab-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="05eab-131">Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido.</span><span class="sxs-lookup"><span data-stu-id="05eab-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="05eab-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="05eab-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="05eab-133">Codifica anexos no modo de único Apple do Macintosh.</span><span class="sxs-lookup"><span data-stu-id="05eab-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="05eab-134">Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido.</span><span class="sxs-lookup"><span data-stu-id="05eab-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="05eab-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="05eab-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="05eab-136">Codifica anexos no UUENCODE do Macintosh.</span><span class="sxs-lookup"><span data-stu-id="05eab-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="05eab-137">Se o sinalizador ENCODING_MIME for definido, esse sinalizador será ignorado e será usada a codificação BinHex.</span><span class="sxs-lookup"><span data-stu-id="05eab-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="05eab-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="05eab-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05eab-139">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="05eab-139">Protocol specifications</span></span>

<span data-ttu-id="05eab-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05eab-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05eab-141">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="05eab-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05eab-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05eab-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05eab-143">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="05eab-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="05eab-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05eab-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05eab-145">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="05eab-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="05eab-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05eab-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05eab-147">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="05eab-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="05eab-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05eab-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05eab-149">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="05eab-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05eab-150">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="05eab-150">Header files</span></span>

<span data-ttu-id="05eab-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05eab-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="05eab-152">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="05eab-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="05eab-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05eab-153">Mapitags.h</span></span>
  
> <span data-ttu-id="05eab-154">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="05eab-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05eab-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="05eab-155">See also</span></span>



[<span data-ttu-id="05eab-156">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="05eab-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05eab-157">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="05eab-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05eab-158">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="05eab-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05eab-159">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="05eab-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

