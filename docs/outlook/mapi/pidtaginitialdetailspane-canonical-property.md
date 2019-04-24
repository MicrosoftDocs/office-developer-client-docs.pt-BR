---
title: Propriedade canônica PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3bf0f52dbeda37ac35024ae3bf38df8919e37b60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346575"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="d4e82-103">Propriedade canônica PidTagInitialDetailsPane</span><span class="sxs-lookup"><span data-stu-id="d4e82-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="d4e82-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4e82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4e82-105">Indica a página de um modelo de exibição a ser exibida primeiro.</span><span class="sxs-lookup"><span data-stu-id="d4e82-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4e82-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d4e82-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4e82-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="d4e82-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="d4e82-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d4e82-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4e82-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="d4e82-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="d4e82-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d4e82-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4e82-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d4e82-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d4e82-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d4e82-112">Area:</span></span>  <br/> |<span data-ttu-id="d4e82-113">Tabelas de exibição MAPI</span><span class="sxs-lookup"><span data-stu-id="d4e82-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4e82-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4e82-114">Remarks</span></span>

<span data-ttu-id="d4e82-115">Ele deve estar presente em todos os objetos do catálogo de endereços em um servidor de interface de provedor de serviços de nome (NSPI) e deve ter o valor zero (0).</span><span class="sxs-lookup"><span data-stu-id="d4e82-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="d4e82-116">Ele não deve ser definido para qualquer objeto em um catálogo de endereços offline.</span><span class="sxs-lookup"><span data-stu-id="d4e82-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4e82-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4e82-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4e82-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="d4e82-118">Protocol specifications</span></span>

<span data-ttu-id="d4e82-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4e82-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4e82-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d4e82-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4e82-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4e82-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4e82-122">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="d4e82-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4e82-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d4e82-123">Header files</span></span>

<span data-ttu-id="d4e82-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d4e82-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4e82-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d4e82-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4e82-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d4e82-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d4e82-127">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="d4e82-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4e82-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4e82-128">See also</span></span>



[<span data-ttu-id="d4e82-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d4e82-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4e82-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d4e82-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4e82-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d4e82-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4e82-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d4e82-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

