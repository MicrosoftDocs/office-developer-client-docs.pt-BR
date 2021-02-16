---
title: Propriedade canônica PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429247"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="52575-103">Propriedade canônica PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="52575-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="52575-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52575-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52575-105">Contém sinalizadores que indicam se os provedores darão suporte a vários endereços de email por item de contato.</span><span class="sxs-lookup"><span data-stu-id="52575-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52575-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="52575-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52575-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="52575-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="52575-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="52575-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52575-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="52575-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="52575-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="52575-110">Data type:</span></span>  <br/> |<span data-ttu-id="52575-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="52575-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="52575-112">Área:</span><span class="sxs-lookup"><span data-stu-id="52575-112">Area:</span></span>  <br/> |<span data-ttu-id="52575-113">Contact address book</span><span class="sxs-lookup"><span data-stu-id="52575-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52575-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="52575-114">Remarks</span></span>

<span data-ttu-id="52575-115">Se os sinalizadores dessa propriedade são VERDADEIROs, o provedor não inclui contatos sem endereços de email.</span><span class="sxs-lookup"><span data-stu-id="52575-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="52575-116">Somente o endereço de email principal será aumente.</span><span class="sxs-lookup"><span data-stu-id="52575-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="52575-117">Esta é uma propriedade em uma seção de perfil do Livro de Endereços de Contato.</span><span class="sxs-lookup"><span data-stu-id="52575-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52575-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="52575-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="52575-119">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="52575-119">Header files</span></span>

<span data-ttu-id="52575-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52575-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="52575-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="52575-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="52575-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52575-122">Mapitags.h</span></span>
  
> <span data-ttu-id="52575-123">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="52575-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52575-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="52575-124">See also</span></span>



[<span data-ttu-id="52575-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="52575-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52575-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="52575-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52575-127">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="52575-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52575-128">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="52575-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

