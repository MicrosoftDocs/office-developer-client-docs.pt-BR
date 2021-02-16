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
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342669"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="74127-103">Propriedade canônica PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="74127-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="74127-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74127-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74127-105">Contém uma máscara de bits de preferências de codificação.</span><span class="sxs-lookup"><span data-stu-id="74127-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74127-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="74127-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74127-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="74127-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="74127-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74127-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74127-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="74127-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="74127-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="74127-110">Data type:</span></span>  <br/> |<span data-ttu-id="74127-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74127-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74127-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74127-112">Area:</span></span>  <br/> |<span data-ttu-id="74127-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="74127-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74127-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="74127-114">Remarks</span></span>

<span data-ttu-id="74127-115">De definir essa propriedade para indicar as opções de codificação usadas.</span><span class="sxs-lookup"><span data-stu-id="74127-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="74127-116">Essa propriedade contém os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="74127-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="74127-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="74127-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="74127-118">Codificar o texto da mensagem em HTML.</span><span class="sxs-lookup"><span data-stu-id="74127-118">Encode the message text in HTML.</span></span> <span data-ttu-id="74127-119">Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido.</span><span class="sxs-lookup"><span data-stu-id="74127-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74127-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="74127-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="74127-121">Codificar o texto da mensagem usando texto e HTML como alternativas de várias partes do MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="74127-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="74127-122">Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido.</span><span class="sxs-lookup"><span data-stu-id="74127-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74127-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="74127-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="74127-124">Codificar a mensagem usando MIME.</span><span class="sxs-lookup"><span data-stu-id="74127-124">Encode the message using MIME.</span></span> <span data-ttu-id="74127-125">Se esse sinalizador não estiver definido, MAPI codifica o texto da mensagem em texto sem código e os anexos em UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="74127-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="74127-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="74127-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="74127-127">Use os outros sinalizadores nesta máscara de bits para determinar a codificação.</span><span class="sxs-lookup"><span data-stu-id="74127-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="74127-128">Se esse sinalizador não estiver definido, o MAPI o deixará no sistema de mensagens para tomar decisões de codificação.</span><span class="sxs-lookup"><span data-stu-id="74127-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="74127-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="74127-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="74127-130">Codificar anexos do Macintosh no modo duplo da Apple.</span><span class="sxs-lookup"><span data-stu-id="74127-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="74127-131">Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido.</span><span class="sxs-lookup"><span data-stu-id="74127-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74127-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="74127-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="74127-133">Codificar anexos do Macintosh no modo único da Apple.</span><span class="sxs-lookup"><span data-stu-id="74127-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="74127-134">Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido.</span><span class="sxs-lookup"><span data-stu-id="74127-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74127-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="74127-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="74127-136">Codificar anexos do Macintosh em UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="74127-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="74127-137">Se o ENCODING_MIME sinalizador estiver definido, esse sinalizador será ignorado e a codificação BinHex será usada.</span><span class="sxs-lookup"><span data-stu-id="74127-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="74127-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74127-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74127-139">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="74127-139">Protocol specifications</span></span>

<span data-ttu-id="74127-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74127-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74127-141">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="74127-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74127-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74127-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74127-143">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="74127-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="74127-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74127-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74127-145">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="74127-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="74127-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74127-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74127-147">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="74127-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="74127-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74127-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74127-149">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="74127-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74127-150">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="74127-150">Header files</span></span>

<span data-ttu-id="74127-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74127-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="74127-152">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="74127-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="74127-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74127-153">Mapitags.h</span></span>
  
> <span data-ttu-id="74127-154">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="74127-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74127-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="74127-155">See also</span></span>



[<span data-ttu-id="74127-156">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74127-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74127-157">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="74127-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74127-158">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="74127-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74127-159">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="74127-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

