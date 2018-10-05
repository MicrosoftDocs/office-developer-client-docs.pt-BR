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
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395697"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="49148-103">Propriedade canônica PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="49148-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="49148-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49148-105">Contém o valor do campo de cabeçalho de referências de uma mensagem email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="49148-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49148-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="49148-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49148-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="49148-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="49148-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="49148-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49148-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="49148-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="49148-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="49148-110">Data type:</span></span>  <br/> |<span data-ttu-id="49148-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49148-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="49148-112">Área:</span><span class="sxs-lookup"><span data-stu-id="49148-112">Area:</span></span>  <br/> |<span data-ttu-id="49148-113">MIME</span><span class="sxs-lookup"><span data-stu-id="49148-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49148-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="49148-114">Remarks</span></span>

<span data-ttu-id="49148-115">Para gerar um campo de cabeçalho de referências, os clientes devem definir essas propriedades para o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="49148-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="49148-116">Os autores MIME devem copiar o valor dessas propriedades no campo de cabeçalho de referências.</span><span class="sxs-lookup"><span data-stu-id="49148-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="49148-117">Para definir o valor dessas propriedades, os clientes MIME devem gravar o valor desejado a um campo de cabeçalho de referências.</span><span class="sxs-lookup"><span data-stu-id="49148-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="49148-118">Leitores MIME devem copiar o valor do campo de cabeçalho de referências a essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="49148-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="49148-119">Leitores MIME podem truncar o valor dessas propriedades se ela exceder 64KB de comprimento.</span><span class="sxs-lookup"><span data-stu-id="49148-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49148-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="49148-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49148-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="49148-121">Protocol specifications</span></span>

<span data-ttu-id="49148-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49148-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49148-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49148-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49148-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49148-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49148-125">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="49148-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49148-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49148-126">Header files</span></span>

<span data-ttu-id="49148-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49148-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="49148-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="49148-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="49148-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="49148-129">Mapitags.h</span></span>
  
> <span data-ttu-id="49148-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="49148-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49148-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="49148-131">See also</span></span>



[<span data-ttu-id="49148-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="49148-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49148-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="49148-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49148-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="49148-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49148-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="49148-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

