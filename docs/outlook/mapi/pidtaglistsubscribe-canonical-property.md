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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279654"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="e72b5-103">Propriedade canônica PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="e72b5-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="e72b5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e72b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e72b5-105">Contém o valor de uma mensagem MIME (Multipurpose Internet Mail Extensions) List-Subscribe de texto.</span><span class="sxs-lookup"><span data-stu-id="e72b5-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e72b5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e72b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e72b5-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="e72b5-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="e72b5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e72b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e72b5-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="e72b5-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="e72b5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e72b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="e72b5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e72b5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e72b5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e72b5-112">Area:</span></span>  <br/> |<span data-ttu-id="e72b5-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="e72b5-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e72b5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e72b5-114">Remarks</span></span>

<span data-ttu-id="e72b5-115">Para gerar um List-Subscribe de List-Subscribe, os clientes devem definir o valor dessas propriedades como o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="e72b5-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="e72b5-116">Os autores MIME devem copiar o valor dessas propriedades para o List-Subscribe de texto.</span><span class="sxs-lookup"><span data-stu-id="e72b5-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="e72b5-117">Para definir o valor de propriedades relacionadas ao servidor como estas, os clientes MIME devem gravar os campos de header conforme especificado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e72b5-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="e72b5-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="e72b5-118">**Property**</span></span>|<span data-ttu-id="e72b5-119">**Nome do campo de header preferencial**</span><span class="sxs-lookup"><span data-stu-id="e72b5-119">**Preferred header field name**</span></span>|<span data-ttu-id="e72b5-120">**Nome do campo de header alternativo**</span><span class="sxs-lookup"><span data-stu-id="e72b5-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e72b5-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="e72b5-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="e72b5-122">List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="e72b5-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="e72b5-123">X-List-Subscribe</span><span class="sxs-lookup"><span data-stu-id="e72b5-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e72b5-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e72b5-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e72b5-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e72b5-125">Protocol specifications</span></span>

<span data-ttu-id="e72b5-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e72b5-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e72b5-127">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e72b5-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e72b5-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e72b5-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e72b5-129">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e72b5-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e72b5-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e72b5-130">Header files</span></span>

<span data-ttu-id="e72b5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e72b5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e72b5-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e72b5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e72b5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e72b5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e72b5-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e72b5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e72b5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="e72b5-135">See also</span></span>



[<span data-ttu-id="e72b5-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e72b5-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e72b5-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e72b5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e72b5-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e72b5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e72b5-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e72b5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

