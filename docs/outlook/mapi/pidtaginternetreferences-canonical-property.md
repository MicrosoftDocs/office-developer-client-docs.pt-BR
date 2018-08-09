---
title: Propriedade canônica PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4558fcdba11aed92eb21972ed62320209ade77ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769377"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="59918-103">Propriedade canônica PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="59918-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="59918-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59918-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59918-105">Contém o valor do campo de cabeçalho de referências de uma mensagem email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="59918-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59918-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="59918-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59918-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="59918-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="59918-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="59918-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59918-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="59918-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="59918-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="59918-110">Data type:</span></span>  <br/> |<span data-ttu-id="59918-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="59918-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="59918-112">Área:</span><span class="sxs-lookup"><span data-stu-id="59918-112">Area:</span></span>  <br/> |<span data-ttu-id="59918-113">MIME</span><span class="sxs-lookup"><span data-stu-id="59918-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59918-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="59918-114">Remarks</span></span>

<span data-ttu-id="59918-115">Para gerar um campo de cabeçalho de referências, os clientes devem definir essas propriedades para o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="59918-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="59918-116">Os autores MIME devem copiar o valor dessas propriedades no campo de cabeçalho de referências.</span><span class="sxs-lookup"><span data-stu-id="59918-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="59918-117">Para definir o valor dessas propriedades, os clientes MIME devem gravar o valor desejado a um campo de cabeçalho de referências.</span><span class="sxs-lookup"><span data-stu-id="59918-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="59918-118">Leitores MIME devem copiar o valor do campo de cabeçalho de referências a essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="59918-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="59918-119">Leitores MIME podem truncar o valor dessas propriedades se ela exceder 64KB de comprimento.</span><span class="sxs-lookup"><span data-stu-id="59918-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59918-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="59918-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59918-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="59918-121">Protocol specifications</span></span>

<span data-ttu-id="59918-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59918-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59918-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="59918-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59918-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59918-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59918-125">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="59918-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59918-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="59918-126">Header files</span></span>

<span data-ttu-id="59918-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59918-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="59918-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="59918-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="59918-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59918-129">Mapitags.h</span></span>
  
> <span data-ttu-id="59918-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="59918-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59918-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="59918-131">See also</span></span>



[<span data-ttu-id="59918-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="59918-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59918-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="59918-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59918-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="59918-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59918-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="59918-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
