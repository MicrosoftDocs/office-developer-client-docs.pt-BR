---
title: Propriedade canônica PidTagBodyContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 90a873174b5b990f165d0b2173efa38fc7df2d9d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394913"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="bc121-103">Propriedade canônica PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="bc121-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="bc121-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc121-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc121-105">Contém o valor de um campo de cabeçalho de conteúdo MIME-local.</span><span class="sxs-lookup"><span data-stu-id="bc121-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc121-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bc121-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc121-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="bc121-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="bc121-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bc121-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc121-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="bc121-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="bc121-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bc121-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc121-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc121-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bc121-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bc121-112">Area:</span></span>  <br/> |<span data-ttu-id="bc121-113">MIME</span><span class="sxs-lookup"><span data-stu-id="bc121-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc121-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc121-114">Remarks</span></span>

<span data-ttu-id="bc121-115">Para definir o valor dessas propriedades, os clientes MIME devem gravar o valor desejado um campo de cabeçalho de local de conteúdo em uma entidade MIME que mapeie para o corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc121-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="bc121-116">Leitores MIME devem copiar o valor de um campo de cabeçalho de local de conteúdo em uma entidade MIME tais como o valor dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bc121-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc121-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc121-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc121-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bc121-118">Protocol specifications</span></span>

<span data-ttu-id="bc121-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc121-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc121-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bc121-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc121-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc121-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc121-122">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc121-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc121-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bc121-123">Header files</span></span>

<span data-ttu-id="bc121-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc121-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc121-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bc121-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc121-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc121-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bc121-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bc121-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc121-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc121-128">See also</span></span>



[<span data-ttu-id="bc121-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bc121-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc121-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bc121-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc121-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bc121-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc121-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bc121-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

