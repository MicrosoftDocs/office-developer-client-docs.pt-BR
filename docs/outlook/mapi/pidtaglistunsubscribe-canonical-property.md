---
title: Propriedade canônica PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278875"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="3d0bd-103">Propriedade canônica PidTagListUnsubscribe</span><span class="sxs-lookup"><span data-stu-id="3d0bd-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="3d0bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d0bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d0bd-105">Contém o valor de uma mensagem MIME (Multipurpose Internet Mail Extensions) List-Unsubscribe de texto.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d0bd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3d0bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d0bd-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="3d0bd-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="3d0bd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3d0bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d0bd-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="3d0bd-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="3d0bd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3d0bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d0bd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3d0bd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3d0bd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3d0bd-112">Area:</span></span>  <br/> |<span data-ttu-id="3d0bd-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="3d0bd-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d0bd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d0bd-114">Remarks</span></span>

<span data-ttu-id="3d0bd-115">Para gerar um List-Unsubscribe de List-Unsubscribe, os clientes devem definir essas propriedades com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="3d0bd-116">Os autores MIME devem copiar o valor dessas propriedades para o List-Unsubscribe de texto.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="3d0bd-117">Para definir o valor dessas propriedades relacionadas ao servidor de lista, os clientes MIME devem gravar os campos de header conforme especificado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="3d0bd-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="3d0bd-118">**Property**</span></span>|<span data-ttu-id="3d0bd-119">**Nome do campo de header preferencial**</span><span class="sxs-lookup"><span data-stu-id="3d0bd-119">**Preferred header field name**</span></span>|<span data-ttu-id="3d0bd-120">**Nome do campo de header alternativo**</span><span class="sxs-lookup"><span data-stu-id="3d0bd-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3d0bd-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="3d0bd-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="3d0bd-122">List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="3d0bd-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="3d0bd-123">X-List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="3d0bd-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3d0bd-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d0bd-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d0bd-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3d0bd-125">Protocol specifications</span></span>

<span data-ttu-id="3d0bd-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0bd-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0bd-127">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d0bd-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0bd-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0bd-129">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d0bd-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3d0bd-130">Header files</span></span>

<span data-ttu-id="3d0bd-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d0bd-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d0bd-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d0bd-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d0bd-133">Mapitags.h</span></span>
  
> <span data-ttu-id="3d0bd-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3d0bd-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d0bd-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d0bd-135">See also</span></span>



[<span data-ttu-id="3d0bd-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3d0bd-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d0bd-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3d0bd-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d0bd-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3d0bd-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d0bd-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3d0bd-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

