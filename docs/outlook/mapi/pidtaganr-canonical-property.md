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
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327962"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="8f8ae-103">Propriedade canônica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="8f8ae-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="8f8ae-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f8ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f8ae-105">Contém um valor de cadeia de caracteres para uso em uma restrição de propriedade em uma tabela de conteúdo de contêiner do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f8ae-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8f8ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f8ae-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="8f8ae-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="8f8ae-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8f8ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f8ae-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="8f8ae-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="8f8ae-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8f8ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f8ae-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8f8ae-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8f8ae-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8f8ae-112">Area:</span></span>  <br/> |<span data-ttu-id="8f8ae-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="8f8ae-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f8ae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f8ae-114">Remarks</span></span>

<span data-ttu-id="8f8ae-115">Essas propriedades não pertencem a nenhum objeto; é fornecida pelos provedores de agendamento de endereços [em estruturas SPropertyRestriction.](spropertyrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="8f8ae-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="8f8ae-116">Essa propriedade contém uma cadeia de caracteres ANR (resolução de nomes ambíguos) que pode ser testada em relação à tabela de conteúdo de um contêiner de agenda de endereços para encontrar destinatários de mensagem correspondentes.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="8f8ae-117">Os provedores de agendas coincidem com o **valor PR_ANR** propriedades associadas e de cada entrada na tabela de conteúdo, usando um algoritmo de correspondência definido pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="8f8ae-118">As colunas usadas nessa combinação são escolhidas pelo provedor como parte do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="8f8ae-119">A **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é a mais usada; a **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) também é útil quando contém o nome de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="8f8ae-120">Para obter mais informações sobre resolução de nomes ambíguos, consulte [Restrições do Address Book](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="8f8ae-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8f8ae-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f8ae-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f8ae-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8f8ae-122">Protocol specifications</span></span>

<span data-ttu-id="8f8ae-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f8ae-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f8ae-124">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f8ae-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f8ae-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f8ae-126">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f8ae-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="8f8ae-127">Header files</span></span>

<span data-ttu-id="8f8ae-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f8ae-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f8ae-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f8ae-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8f8ae-130">Mapitags.h</span></span>
  
> <span data-ttu-id="8f8ae-131">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8f8ae-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f8ae-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f8ae-132">See also</span></span>



[<span data-ttu-id="8f8ae-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="8f8ae-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="8f8ae-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="8f8ae-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="8f8ae-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8f8ae-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f8ae-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8f8ae-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f8ae-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8f8ae-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f8ae-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8f8ae-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

