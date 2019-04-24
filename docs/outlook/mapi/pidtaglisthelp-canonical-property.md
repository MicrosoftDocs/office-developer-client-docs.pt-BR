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
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="16ebf-103">Propriedade canônica PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="16ebf-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="16ebf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16ebf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16ebf-105">Contém o valor de um campo de cabeçalho da ajuda de lista de mensagens de MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="16ebf-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16ebf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="16ebf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16ebf-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="16ebf-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="16ebf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="16ebf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16ebf-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="16ebf-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="16ebf-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="16ebf-110">Data type:</span></span>  <br/> |<span data-ttu-id="16ebf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16ebf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="16ebf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="16ebf-112">Area:</span></span>  <br/> |<span data-ttu-id="16ebf-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="16ebf-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16ebf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="16ebf-114">Remarks</span></span>

<span data-ttu-id="16ebf-115">Para gerar um campo de cabeçalho List-Help, os clientes devem definir o valor de **PR_LIST_HELP** ou uma propriedade associada para o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="16ebf-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="16ebf-116">Os gravadores MIME devem copiar esse valor para o campo de cabeçalho List-help.</span><span class="sxs-lookup"><span data-stu-id="16ebf-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="16ebf-117">Para definir o valor dessas propriedades relacionadas ao servidor de lista, os clientes MIME devem gravar os campos de cabeçalho conforme especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="16ebf-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="16ebf-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="16ebf-118">**Property**</span></span>|<span data-ttu-id="16ebf-119">**Nome do campo de cabeçalho preferencial**</span><span class="sxs-lookup"><span data-stu-id="16ebf-119">**Preferred header field name**</span></span>|<span data-ttu-id="16ebf-120">**Nome do campo de cabeçalho alternativo**</span><span class="sxs-lookup"><span data-stu-id="16ebf-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16ebf-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="16ebf-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="16ebf-122">Lista-ajuda</span><span class="sxs-lookup"><span data-stu-id="16ebf-122">List-Help</span></span>  <br/> |<span data-ttu-id="16ebf-123">Lista de X-ajuda</span><span class="sxs-lookup"><span data-stu-id="16ebf-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="16ebf-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="16ebf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16ebf-125">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="16ebf-125">Protocol specifications</span></span>

<span data-ttu-id="16ebf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16ebf-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16ebf-127">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="16ebf-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="16ebf-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16ebf-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16ebf-129">Converte as convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="16ebf-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="16ebf-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="16ebf-130">Header files</span></span>

<span data-ttu-id="16ebf-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="16ebf-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="16ebf-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="16ebf-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="16ebf-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="16ebf-133">Mapitags.h</span></span>
  
> <span data-ttu-id="16ebf-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="16ebf-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16ebf-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="16ebf-135">See also</span></span>



[<span data-ttu-id="16ebf-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="16ebf-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16ebf-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="16ebf-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16ebf-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="16ebf-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16ebf-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="16ebf-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

