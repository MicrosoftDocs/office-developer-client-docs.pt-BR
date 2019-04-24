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
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358818"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="6f894-103">Propriedade canônica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="6f894-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="6f894-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f894-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f894-105">Contém o **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expresso como um formato de ID de entrada permanente.</span><span class="sxs-lookup"><span data-stu-id="6f894-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f894-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6f894-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f894-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="6f894-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="6f894-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6f894-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f894-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="6f894-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="6f894-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6f894-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f894-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6f894-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6f894-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6f894-112">Area:</span></span>  <br/> |<span data-ttu-id="6f894-113">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="6f894-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f894-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f894-114">Remarks</span></span>

<span data-ttu-id="6f894-115">Esse valor deve estar presente para todos os objetos do catálogo de endereços em um servidor de interface de provedor de serviços de nome (NSPI), o nome diferenciado (DN) deve corresponder ao valor de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e seu DN deve seguir o formato DN especificação específica para o tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="6f894-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="6f894-116">Essa propriedade não está presente nos objetos de um catálogo de endereços offline.</span><span class="sxs-lookup"><span data-stu-id="6f894-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f894-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f894-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f894-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="6f894-118">Protocol specifications</span></span>

<span data-ttu-id="6f894-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f894-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f894-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6f894-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f894-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f894-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f894-122">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="6f894-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f894-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f894-123">Header files</span></span>

<span data-ttu-id="6f894-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6f894-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f894-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6f894-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f894-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6f894-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6f894-127">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="6f894-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f894-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f894-128">See also</span></span>



[<span data-ttu-id="6f894-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6f894-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f894-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6f894-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f894-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6f894-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f894-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6f894-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

