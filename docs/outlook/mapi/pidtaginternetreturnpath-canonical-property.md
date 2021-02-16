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
ms.openlocfilehash: c2d8eaf627f789c3e862a83d71e4ca2e3e55e1e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327955"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="6dd60-103">Propriedade canônica PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="6dd60-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="6dd60-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dd60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dd60-105">Contém o valor de uma mensagem MIME (Multipurpose Internet Mail Extensions) Return-Path de texto.</span><span class="sxs-lookup"><span data-stu-id="6dd60-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="6dd60-106">O endereço de email do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6dd60-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6dd60-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6dd60-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="6dd60-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="6dd60-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="6dd60-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6dd60-109">Identifier:</span></span>  <br/> |<span data-ttu-id="6dd60-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="6dd60-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="6dd60-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6dd60-111">Data type:</span></span>  <br/> |<span data-ttu-id="6dd60-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6dd60-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6dd60-113">Área:</span><span class="sxs-lookup"><span data-stu-id="6dd60-113">Area:</span></span>  <br/> |<span data-ttu-id="6dd60-114">MIME</span><span class="sxs-lookup"><span data-stu-id="6dd60-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dd60-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dd60-115">Remarks</span></span>

<span data-ttu-id="6dd60-116">Para recuperar o valor dessa propriedade, primeiro use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique essa marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="6dd60-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="6dd60-117">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a [estrutura MAPINAMEID](mapinameid.md) apontada pelo parâmetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="6dd60-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6dd60-118">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="6dd60-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="6dd60-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="6dd60-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="6dd60-120">ulKind:</span><span class="sxs-lookup"><span data-stu-id="6dd60-120">ulKind:</span></span>  <br/> |<span data-ttu-id="6dd60-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="6dd60-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="6dd60-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="6dd60-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="6dd60-123">L"return-path"</span><span class="sxs-lookup"><span data-stu-id="6dd60-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6dd60-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6dd60-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6dd60-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6dd60-125">Protocol specifications</span></span>

<span data-ttu-id="6dd60-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dd60-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dd60-127">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6dd60-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6dd60-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dd60-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dd60-129">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="6dd60-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6dd60-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="6dd60-130">Header files</span></span>

<span data-ttu-id="6dd60-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dd60-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="6dd60-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6dd60-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="6dd60-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6dd60-133">Mapitags.h</span></span>
  
> <span data-ttu-id="6dd60-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6dd60-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6dd60-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dd60-135">See also</span></span>



[<span data-ttu-id="6dd60-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6dd60-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6dd60-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6dd60-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6dd60-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6dd60-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6dd60-139">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6dd60-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6dd60-140">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6dd60-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

