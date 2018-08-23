---
title: Propriedade canônica PidTagOriginalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eab72c5b49ba501d8ab5516bf5a5eae9ea82abe0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588703"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="f84a2-103">Propriedade canônica PidTagOriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="f84a2-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f84a2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f84a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f84a2-105">Contém o identificador de entrada original para uma entrada copiada de um catálogo de endereços a um catálogo de endereços pessoais ou outro catálogo de endereços gravável.</span><span class="sxs-lookup"><span data-stu-id="f84a2-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f84a2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f84a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f84a2-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f84a2-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f84a2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f84a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f84a2-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="f84a2-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="f84a2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f84a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="f84a2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f84a2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f84a2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f84a2-112">Area:</span></span>  <br/> |<span data-ttu-id="f84a2-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="f84a2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f84a2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f84a2-114">Remarks</span></span>

<span data-ttu-id="f84a2-115">Essa propriedade é uma das propriedades que contêm informações sobre a fonte original de uma entrada copiada.</span><span class="sxs-lookup"><span data-stu-id="f84a2-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="f84a2-116">Para um relatório nonread, essa propriedade contém uma cópia do identificador de entrada do remetente da mensagem original para o qual o relatório é gerado.</span><span class="sxs-lookup"><span data-stu-id="f84a2-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="f84a2-117">Quando o destinatário original fizer parte de uma lista de distribuição, o identificador de entrada da lista de distribuição é preservado para o relatório.</span><span class="sxs-lookup"><span data-stu-id="f84a2-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f84a2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f84a2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f84a2-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f84a2-119">Protocol specifications</span></span>

<span data-ttu-id="f84a2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f84a2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f84a2-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f84a2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f84a2-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f84a2-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f84a2-123">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="f84a2-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="f84a2-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f84a2-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f84a2-125">Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="f84a2-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f84a2-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f84a2-126">Header files</span></span>

<span data-ttu-id="f84a2-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f84a2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f84a2-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f84a2-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="f84a2-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f84a2-129">Mapitags.h</span></span>
  
> <span data-ttu-id="f84a2-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f84a2-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f84a2-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f84a2-131">See also</span></span>



[<span data-ttu-id="f84a2-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f84a2-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f84a2-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f84a2-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f84a2-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f84a2-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f84a2-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f84a2-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

