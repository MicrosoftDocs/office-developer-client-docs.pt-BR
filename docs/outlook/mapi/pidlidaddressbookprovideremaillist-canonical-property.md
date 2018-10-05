---
title: Propriedade canônica PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390356"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="d6ebd-103">Propriedade canônica PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="d6ebd-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="d6ebd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6ebd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6ebd-105">Especifica quais propriedades de endereço eletrônico estão definidas no contato.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6ebd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d6ebd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6ebd-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="d6ebd-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="d6ebd-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="d6ebd-108">Property set:</span></span>  <br/> |<span data-ttu-id="d6ebd-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="d6ebd-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="d6ebd-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="d6ebd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d6ebd-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="d6ebd-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="d6ebd-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d6ebd-112">Data type:</span></span>  <br/> |<span data-ttu-id="d6ebd-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d6ebd-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="d6ebd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d6ebd-114">Area:</span></span>  <br/> |<span data-ttu-id="d6ebd-115">Contato</span><span class="sxs-lookup"><span data-stu-id="d6ebd-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6ebd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6ebd-116">Remarks</span></span>

<span data-ttu-id="d6ebd-117">Cada valor PT_LONG desta propriedade deve ser exclusiva na propriedade e deve ser definida como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="d6ebd-118">Se essa propriedade estiver definida, a propriedade **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) também deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="d6ebd-119">Essas duas propriedades devem ser mantidas sincronizadas entre si.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="d6ebd-120">Por exemplo, se um dos valores em **dispidABPEmailList** for "0x00000000", em seguida, **dispidABPArrayType** deve ter o bit "0x00000001" definido.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="d6ebd-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d6ebd-121">**Value**</span></span>|<span data-ttu-id="d6ebd-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d6ebd-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6ebd-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d6ebd-123">0x00000000</span></span>  <br/> |<span data-ttu-id="d6ebd-124">Email1 é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d6ebd-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d6ebd-125">0x00000001</span></span>  <br/> |<span data-ttu-id="d6ebd-126">Email2 é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d6ebd-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d6ebd-127">0x00000002</span></span>  <br/> |<span data-ttu-id="d6ebd-128">Email3 é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d6ebd-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="d6ebd-129">0x00000003</span></span>  <br/> |<span data-ttu-id="d6ebd-130">Fax comercial é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d6ebd-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d6ebd-131">0x00000004</span></span>  <br/> |<span data-ttu-id="d6ebd-132">Fax residencial é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="d6ebd-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="d6ebd-133">0x00000005</span></span>  <br/> |<span data-ttu-id="d6ebd-134">Fax principal é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d6ebd-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6ebd-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6ebd-136">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d6ebd-136">Protocol specifications</span></span>

<span data-ttu-id="d6ebd-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6ebd-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6ebd-138">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6ebd-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6ebd-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6ebd-140">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6ebd-141">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d6ebd-141">Header files</span></span>

<span data-ttu-id="d6ebd-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6ebd-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6ebd-143">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d6ebd-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6ebd-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6ebd-144">See also</span></span>



[<span data-ttu-id="d6ebd-145">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ebd-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6ebd-146">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d6ebd-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6ebd-147">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ebd-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6ebd-148">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d6ebd-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

