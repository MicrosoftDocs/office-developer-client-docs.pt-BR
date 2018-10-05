---
title: Propriedade canônica PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387206"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="5341b-103">Propriedade canônica PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="5341b-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="5341b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5341b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5341b-105">Contém o valor do campo de cabeçalho de uma mensagem de email extensões MIME (Multipurpose Internet) ajuda a lista.</span><span class="sxs-lookup"><span data-stu-id="5341b-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5341b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5341b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5341b-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="5341b-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="5341b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5341b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5341b-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="5341b-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="5341b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5341b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5341b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5341b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5341b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5341b-112">Area:</span></span>  <br/> |<span data-ttu-id="5341b-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="5341b-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5341b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5341b-114">Remarks</span></span>

<span data-ttu-id="5341b-115">Para gerar um campo de cabeçalho de lista-Help, clientes devem definir o valor de **PR_LIST_HELP** ou uma propriedade associada com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="5341b-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="5341b-116">Os autores MIME devem copiar esse valor no campo de cabeçalho de lista-Help.</span><span class="sxs-lookup"><span data-stu-id="5341b-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="5341b-117">Para definir o valor dessas propriedades relacionadas ao servidor de lista, os clientes MIME devem gravar os campos de cabeçalho, conforme especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="5341b-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="5341b-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="5341b-118">**Property**</span></span>|<span data-ttu-id="5341b-119">**Nome do campo de cabeçalho preferencial**</span><span class="sxs-lookup"><span data-stu-id="5341b-119">**Preferred header field name**</span></span>|<span data-ttu-id="5341b-120">**Nome do campo de cabeçalho alternativo**</span><span class="sxs-lookup"><span data-stu-id="5341b-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5341b-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="5341b-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="5341b-122">Lista-Help</span><span class="sxs-lookup"><span data-stu-id="5341b-122">List-Help</span></span>  <br/> |<span data-ttu-id="5341b-123">X-lista-Help</span><span class="sxs-lookup"><span data-stu-id="5341b-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5341b-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5341b-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5341b-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5341b-125">Protocol specifications</span></span>

<span data-ttu-id="5341b-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5341b-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5341b-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5341b-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5341b-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5341b-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5341b-129">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5341b-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5341b-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5341b-130">Header files</span></span>

<span data-ttu-id="5341b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5341b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5341b-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5341b-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5341b-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5341b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5341b-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5341b-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5341b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5341b-135">See also</span></span>



[<span data-ttu-id="5341b-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5341b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5341b-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5341b-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5341b-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5341b-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5341b-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5341b-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

