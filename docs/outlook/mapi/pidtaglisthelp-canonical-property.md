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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279626"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="be9cc-103">Propriedade canônica PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="be9cc-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="be9cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be9cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be9cc-105">Contém o valor de uma mensagem MIME (Multipurpose Internet Mail Extensions) List-Help de texto.</span><span class="sxs-lookup"><span data-stu-id="be9cc-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be9cc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="be9cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be9cc-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="be9cc-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="be9cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be9cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be9cc-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="be9cc-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="be9cc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="be9cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="be9cc-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be9cc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="be9cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="be9cc-112">Area:</span></span>  <br/> |<span data-ttu-id="be9cc-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="be9cc-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be9cc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be9cc-114">Remarks</span></span>

<span data-ttu-id="be9cc-115">Para gerar um List-Help de List-Help, os clientes devem definir o valor de **PR_LIST_HELP** ou uma propriedade associada para o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="be9cc-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="be9cc-116">Os autores MIME devem copiar esse valor para o List-Help de texto.</span><span class="sxs-lookup"><span data-stu-id="be9cc-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="be9cc-117">Para definir o valor dessas propriedades relacionadas ao servidor de lista, os clientes MIME devem gravar os campos de header conforme especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="be9cc-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="be9cc-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="be9cc-118">**Property**</span></span>|<span data-ttu-id="be9cc-119">**Nome do campo de header preferencial**</span><span class="sxs-lookup"><span data-stu-id="be9cc-119">**Preferred header field name**</span></span>|<span data-ttu-id="be9cc-120">**Nome do campo de header alternativo**</span><span class="sxs-lookup"><span data-stu-id="be9cc-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="be9cc-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="be9cc-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="be9cc-122">List-Help</span><span class="sxs-lookup"><span data-stu-id="be9cc-122">List-Help</span></span>  <br/> |<span data-ttu-id="be9cc-123">X-List-Help</span><span class="sxs-lookup"><span data-stu-id="be9cc-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="be9cc-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="be9cc-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be9cc-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="be9cc-125">Protocol specifications</span></span>

<span data-ttu-id="be9cc-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be9cc-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be9cc-127">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="be9cc-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be9cc-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be9cc-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be9cc-129">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="be9cc-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be9cc-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="be9cc-130">Header files</span></span>

<span data-ttu-id="be9cc-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be9cc-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="be9cc-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="be9cc-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="be9cc-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be9cc-133">Mapitags.h</span></span>
  
> <span data-ttu-id="be9cc-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="be9cc-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be9cc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="be9cc-135">See also</span></span>



[<span data-ttu-id="be9cc-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="be9cc-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be9cc-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="be9cc-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be9cc-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="be9cc-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be9cc-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="be9cc-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

