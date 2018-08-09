---
title: Propriedade canônica PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4a43bc33f13d8325a55d09b5ef3031dc632cf587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769551"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="9f553-103">Propriedade canônica PidTagOriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="9f553-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9f553-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f553-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f553-105">Contém o nome de exibição original para uma entrada copiado de um catálogo de endereços para um catálogo de endereços pessoal ou outro catálogo de endereços gravável.</span><span class="sxs-lookup"><span data-stu-id="9f553-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f553-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9f553-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f553-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="9f553-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="9f553-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9f553-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f553-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="9f553-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="9f553-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9f553-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f553-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9f553-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9f553-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9f553-112">Area:</span></span>  <br/> |<span data-ttu-id="9f553-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="9f553-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f553-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f553-114">Remarks</span></span>

<span data-ttu-id="9f553-115">Essas propriedades contêm informações sobre a fonte original de uma entrada copiada.</span><span class="sxs-lookup"><span data-stu-id="9f553-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="9f553-116">Para um relatório nonread, essas propriedades contêm uma cópia do nome para exibição do remetente da mensagem original para o qual o relatório é gerado.</span><span class="sxs-lookup"><span data-stu-id="9f553-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="9f553-117">Quando o destinatário original fizer parte de uma lista de distribuição, o nome para exibição da lista de distribuição é preservado para o relatório.</span><span class="sxs-lookup"><span data-stu-id="9f553-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="9f553-118">Um aplicativo cliente pode utilizar essas propriedades para impedir que a alteração ou "falsificação" das entradas, fornecendo uma cópia inalterada do nome para exibição para comparar.</span><span class="sxs-lookup"><span data-stu-id="9f553-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f553-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f553-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f553-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9f553-120">Protocol specifications</span></span>

<span data-ttu-id="9f553-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f553-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f553-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9f553-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f553-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f553-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f553-124">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="9f553-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f553-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9f553-125">Header files</span></span>

<span data-ttu-id="9f553-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f553-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f553-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9f553-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f553-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9f553-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9f553-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9f553-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f553-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f553-130">See also</span></span>



[<span data-ttu-id="9f553-131">Propriedade canônica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="9f553-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="9f553-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f553-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f553-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9f553-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f553-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9f553-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f553-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9f553-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
