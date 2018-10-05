---
title: Propriedade canônica PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396222"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="9af52-103">Propriedade canônica PidTagMappingSignature</span><span class="sxs-lookup"><span data-stu-id="9af52-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="9af52-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9af52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9af52-105">Contém a assinatura de mapeamento para propriedades nomeadas de um determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="9af52-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9af52-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9af52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9af52-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="9af52-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="9af52-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9af52-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9af52-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="9af52-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="9af52-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9af52-110">Data type:</span></span>  <br/> |<span data-ttu-id="9af52-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9af52-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9af52-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9af52-112">Area:</span></span>  <br/> |<span data-ttu-id="9af52-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="9af52-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9af52-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9af52-114">Remarks</span></span>

<span data-ttu-id="9af52-115">É recomendável que os objetos tendo propriedades nomeadas exponham essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9af52-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="9af52-116">Um aplicativo cliente deve verificar a propriedade **PR_MAPPING_SIGNATURE** dos dois objetos quando copiando nomeada propriedades de um objeto para outro.</span><span class="sxs-lookup"><span data-stu-id="9af52-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="9af52-117">O uso dessa propriedade pode minimizar a conversão entre nomes e os identificadores de propriedades copiadas.</span><span class="sxs-lookup"><span data-stu-id="9af52-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="9af52-118">Se essa propriedade não existe para um determinado objeto MAPI, o objeto tem seu próprio mapeamento exclusivo de nomes e os identificadores.</span><span class="sxs-lookup"><span data-stu-id="9af52-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="9af52-119">Neste caso o cliente deve chamar o método de [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) no objeto de origem e, em seguida, o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) no objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="9af52-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="9af52-120">Quando dois objetos têm o mesmo valor **PR_MAPPING_SIGNATURE** , o cliente não precisará traduzir o nome para o identificador e identificador de nome.</span><span class="sxs-lookup"><span data-stu-id="9af52-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="9af52-121">O cliente pode simplesmente chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) na origem e, em seguida, o método [IMAPIProp::SetProps](imapiprop-setprops.md) no destino.</span><span class="sxs-lookup"><span data-stu-id="9af52-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="9af52-122">Isso é conveniente para clientes que executam copiando personalizado propriedades nomeadas e para provedores Implementando os métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9af52-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="9af52-123">Para obter mais informações sobre propriedades nomeadas e mapeamento de nomes e os identificadores, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9af52-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9af52-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9af52-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9af52-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9af52-125">Protocol specifications</span></span>

<span data-ttu-id="9af52-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9af52-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9af52-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9af52-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9af52-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9af52-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9af52-129">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="9af52-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9af52-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9af52-130">Header files</span></span>

<span data-ttu-id="9af52-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9af52-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9af52-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9af52-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9af52-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9af52-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9af52-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9af52-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9af52-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9af52-135">See also</span></span>



[<span data-ttu-id="9af52-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="9af52-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="9af52-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9af52-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9af52-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9af52-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9af52-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9af52-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9af52-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9af52-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

