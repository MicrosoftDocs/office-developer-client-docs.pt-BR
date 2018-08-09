---
title: Propriedade canônica PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 94e83f4a93bac4ee144c5fbf94fd4b3fdb6c2f55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768941"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="df14b-103">Propriedade canônica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="df14b-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="df14b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df14b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df14b-105">Contém um valor de cadeia de caracteres para uso em uma restrição de propriedade em uma tabela de conteúdo de contêiner de catálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="df14b-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df14b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="df14b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df14b-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="df14b-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="df14b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="df14b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df14b-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="df14b-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="df14b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="df14b-110">Data type:</span></span>  <br/> |<span data-ttu-id="df14b-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="df14b-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="df14b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="df14b-112">Area:</span></span>  <br/> |<span data-ttu-id="df14b-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="df14b-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df14b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="df14b-114">Remarks</span></span>

<span data-ttu-id="df14b-115">Essas propriedades não pertencem a qualquer objeto; ele é fornecido por provedores de catálogo de endereços nas estruturas de [SPropertyRestriction](spropertyrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="df14b-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="df14b-116">Essa propriedade contém uma cadeia de caracteres de (ANR) de resolução de nome ambígua que pode ser testada em relação à tabela de conteúdo de um contêiner catálogo de endereços para localizar os destinatários da mensagem correspondente.</span><span class="sxs-lookup"><span data-stu-id="df14b-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="df14b-117">Provedores de catálogo de endereços correspondem ao valor de **PR_ANR** e propriedades associadas em relação a cada entrada na tabela de conteúdo, usando um algoritmo de correspondência definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="df14b-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="df14b-118">A coluna ou colunas que são usadas nessa correspondência são escolhidas pelo provedor como parte do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="df14b-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="df14b-119">A coluna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é o mais usada; a coluna **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) também é útil quando ela contém o nome de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="df14b-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="df14b-120">Para obter mais informações sobre a resolução de nome ambígua, consulte [Restrições de catálogo de endereços](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="df14b-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df14b-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="df14b-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df14b-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="df14b-122">Protocol specifications</span></span>

<span data-ttu-id="df14b-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df14b-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df14b-124">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="df14b-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df14b-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df14b-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df14b-126">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="df14b-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df14b-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df14b-127">Header files</span></span>

<span data-ttu-id="df14b-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df14b-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="df14b-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="df14b-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="df14b-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df14b-130">Mapitags.h</span></span>
  
> <span data-ttu-id="df14b-131">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="df14b-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df14b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="df14b-132">See also</span></span>



[<span data-ttu-id="df14b-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="df14b-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="df14b-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="df14b-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="df14b-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="df14b-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df14b-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="df14b-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df14b-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="df14b-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df14b-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="df14b-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

