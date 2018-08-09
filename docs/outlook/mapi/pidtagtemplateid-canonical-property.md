---
title: Propriedade canônica PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7672c18f18d39ed1e4e8b4664ba7990563419a20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770122"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="fc3ef-103">Propriedade canônica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="fc3ef-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="fc3ef-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc3ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc3ef-105">Contém o **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressado como um formato de ID de entrada permanente.</span><span class="sxs-lookup"><span data-stu-id="fc3ef-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc3ef-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fc3ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc3ef-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="fc3ef-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="fc3ef-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc3ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc3ef-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="fc3ef-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="fc3ef-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fc3ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc3ef-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc3ef-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc3ef-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc3ef-112">Area:</span></span>  <br/> |<span data-ttu-id="fc3ef-113">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="fc3ef-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc3ef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc3ef-114">Remarks</span></span>

<span data-ttu-id="fc3ef-115">Esse valor deve estar presente para todos os objetos de catálogo de endereços em um servidor de nome serviço provedor NSPI (Interface), seu nome distinto (DN) deve corresponder ao valor de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e seu DN deve seguir o formato do DN especificação determinada para o tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="fc3ef-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="fc3ef-116">Essa propriedade não está presente nos objetos em um catálogo de endereços offline.</span><span class="sxs-lookup"><span data-stu-id="fc3ef-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc3ef-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc3ef-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc3ef-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fc3ef-118">Protocol specifications</span></span>

<span data-ttu-id="fc3ef-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc3ef-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc3ef-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fc3ef-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc3ef-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc3ef-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc3ef-122">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="fc3ef-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc3ef-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fc3ef-123">Header files</span></span>

<span data-ttu-id="fc3ef-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc3ef-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc3ef-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fc3ef-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc3ef-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc3ef-126">Mapitags.h</span></span>
  
> <span data-ttu-id="fc3ef-127">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="fc3ef-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc3ef-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc3ef-128">See also</span></span>



[<span data-ttu-id="fc3ef-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc3ef-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc3ef-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fc3ef-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc3ef-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fc3ef-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc3ef-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fc3ef-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

