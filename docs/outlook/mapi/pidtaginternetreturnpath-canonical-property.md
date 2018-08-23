---
title: Propriedade canônica PidTagInternetReturnPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReturnPath
api_type:
- HeaderDef
ms.assetid: 4530dbcf-9436-4f29-b79e-1bb0f791f60b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3f108ff1053c0aa1046597cd2f11b74bc2dab0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574171"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="ac94f-103">Propriedade canônica PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="ac94f-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="ac94f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac94f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac94f-105">Contém o valor do campo de cabeçalho do caminho de retorno de uma mensagem email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="ac94f-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="ac94f-106">O endereço de email do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac94f-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac94f-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ac94f-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac94f-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="ac94f-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="ac94f-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ac94f-109">Identifier:</span></span>  <br/> |<span data-ttu-id="ac94f-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="ac94f-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="ac94f-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ac94f-111">Data type:</span></span>  <br/> |<span data-ttu-id="ac94f-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac94f-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ac94f-113">Área:</span><span class="sxs-lookup"><span data-stu-id="ac94f-113">Area:</span></span>  <br/> |<span data-ttu-id="ac94f-114">MIME</span><span class="sxs-lookup"><span data-stu-id="ac94f-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac94f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac94f-115">Remarks</span></span>

<span data-ttu-id="ac94f-116">Para recuperar o valor dessa propriedade, primeiro use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="ac94f-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="ac94f-117">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="ac94f-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac94f-118">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="ac94f-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="ac94f-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="ac94f-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="ac94f-120">ulKind:</span><span class="sxs-lookup"><span data-stu-id="ac94f-120">ulKind:</span></span>  <br/> |<span data-ttu-id="ac94f-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="ac94f-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="ac94f-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="ac94f-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="ac94f-123">L "retorno-path"</span><span class="sxs-lookup"><span data-stu-id="ac94f-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ac94f-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac94f-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac94f-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ac94f-125">Protocol specifications</span></span>

<span data-ttu-id="ac94f-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac94f-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac94f-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ac94f-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac94f-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac94f-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac94f-129">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="ac94f-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac94f-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ac94f-130">Header files</span></span>

<span data-ttu-id="ac94f-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac94f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac94f-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ac94f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac94f-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac94f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ac94f-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ac94f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac94f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac94f-135">See also</span></span>



[<span data-ttu-id="ac94f-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ac94f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac94f-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ac94f-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ac94f-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ac94f-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac94f-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ac94f-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac94f-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ac94f-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

