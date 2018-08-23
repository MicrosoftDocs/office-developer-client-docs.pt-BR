---
title: Propriedade canônica PidTagOriginalSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 69108529b13c8c5523f0ea92ef627c69a6722469
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594576"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="4e061-103">Propriedade canônica PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="4e061-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="4e061-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e061-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e061-105">Contém a chave de pesquisa original por uma entrada copiada de um catálogo de endereços a um catálogo de endereços pessoais ou outro catálogo de endereços gravável.</span><span class="sxs-lookup"><span data-stu-id="4e061-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e061-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4e061-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e061-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="4e061-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="4e061-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4e061-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e061-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="4e061-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="4e061-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4e061-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e061-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4e061-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4e061-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4e061-112">Area:</span></span>  <br/> |<span data-ttu-id="4e061-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="4e061-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e061-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e061-114">Remarks</span></span>

<span data-ttu-id="4e061-115">Essa propriedade é uma das propriedades que contêm informações sobre a fonte original de uma entrada copiada.</span><span class="sxs-lookup"><span data-stu-id="4e061-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="4e061-116">Para um relatório nonread, essa propriedade contém uma cópia da chave de pesquisa do remetente da mensagem original para o qual o relatório é gerado.</span><span class="sxs-lookup"><span data-stu-id="4e061-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="4e061-117">Quando o destinatário original fizer parte de uma lista de distribuição, a chave de pesquisa da lista de distribuição é preservada para o relatório.</span><span class="sxs-lookup"><span data-stu-id="4e061-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e061-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e061-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e061-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4e061-119">Protocol specifications</span></span>

<span data-ttu-id="4e061-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e061-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e061-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4e061-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e061-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e061-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e061-123">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="4e061-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e061-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e061-124">Header files</span></span>

<span data-ttu-id="4e061-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e061-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e061-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4e061-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e061-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e061-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4e061-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="4e061-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e061-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e061-129">See also</span></span>



[<span data-ttu-id="4e061-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4e061-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e061-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4e061-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e061-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4e061-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e061-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4e061-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

