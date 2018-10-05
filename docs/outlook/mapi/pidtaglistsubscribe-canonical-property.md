---
title: Propriedade canônica PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389600"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="d5057-103">Propriedade canônica PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="d5057-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="d5057-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5057-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5057-105">Contém o valor do campo de cabeçalho de assinar a lista de uma mensagem de email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="d5057-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5057-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d5057-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5057-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="d5057-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="d5057-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d5057-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d5057-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="d5057-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="d5057-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d5057-110">Data type:</span></span>  <br/> |<span data-ttu-id="d5057-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d5057-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d5057-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d5057-112">Area:</span></span>  <br/> |<span data-ttu-id="d5057-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="d5057-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5057-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5057-114">Remarks</span></span>

<span data-ttu-id="d5057-115">Para gerar um campo de cabeçalho se inscrever lista, os clientes devem definir o valor dessas propriedades com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="d5057-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="d5057-116">Os autores MIME devem copiar o valor dessas propriedades no campo de cabeçalho assine a lista.</span><span class="sxs-lookup"><span data-stu-id="d5057-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="d5057-117">Para definir o valor das propriedades relacionadas ao servidor como essas, os clientes MIME devem gravar os campos de cabeçalho, conforme especificado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5057-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="d5057-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="d5057-118">**Property**</span></span>|<span data-ttu-id="d5057-119">**Nome do campo de cabeçalho preferencial**</span><span class="sxs-lookup"><span data-stu-id="d5057-119">**Preferred header field name**</span></span>|<span data-ttu-id="d5057-120">**Nome do campo de cabeçalho alternativo**</span><span class="sxs-lookup"><span data-stu-id="d5057-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5057-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="d5057-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="d5057-122">Assine a lista</span><span class="sxs-lookup"><span data-stu-id="d5057-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="d5057-123">Inscrever-se lista X</span><span class="sxs-lookup"><span data-stu-id="d5057-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d5057-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5057-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5057-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d5057-125">Protocol specifications</span></span>

<span data-ttu-id="d5057-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5057-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5057-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d5057-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d5057-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5057-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5057-129">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d5057-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d5057-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d5057-130">Header files</span></span>

<span data-ttu-id="d5057-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5057-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5057-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d5057-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d5057-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d5057-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d5057-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d5057-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5057-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5057-135">See also</span></span>



[<span data-ttu-id="d5057-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d5057-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5057-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d5057-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5057-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d5057-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5057-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d5057-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

