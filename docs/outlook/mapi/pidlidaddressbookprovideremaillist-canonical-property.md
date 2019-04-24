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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348479"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="2530b-103">Propriedade canônica PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="2530b-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="2530b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2530b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2530b-105">Especifica quais propriedades de endereço eletrônico estão definidas no contato.</span><span class="sxs-lookup"><span data-stu-id="2530b-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2530b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2530b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2530b-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="2530b-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="2530b-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="2530b-108">Property set:</span></span>  <br/> |<span data-ttu-id="2530b-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="2530b-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="2530b-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2530b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2530b-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="2530b-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="2530b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2530b-112">Data type:</span></span>  <br/> |<span data-ttu-id="2530b-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2530b-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="2530b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2530b-114">Area:</span></span>  <br/> |<span data-ttu-id="2530b-115">Contato</span><span class="sxs-lookup"><span data-stu-id="2530b-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2530b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2530b-116">Remarks</span></span>

<span data-ttu-id="2530b-117">Cada valor de PT_LONG nessa propriedade deve ser exclusivo na propriedade e deve ser definido como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2530b-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="2530b-118">Se essa propriedade for definida, a propriedade **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) também deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="2530b-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="2530b-119">Essas duas propriedades devem ser mantidas sincronizadas umas com as outras.</span><span class="sxs-lookup"><span data-stu-id="2530b-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="2530b-120">Por exemplo, se um dos valores de **dispidABPEmailList** for "0x00000000", **dispidABPArrayType** deverá ter o bit "0x00000001" definido.</span><span class="sxs-lookup"><span data-stu-id="2530b-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="2530b-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2530b-121">**Value**</span></span>|<span data-ttu-id="2530b-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2530b-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2530b-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2530b-123">0x00000000</span></span>  <br/> |<span data-ttu-id="2530b-124">Email1 é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="2530b-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="2530b-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2530b-125">0x00000001</span></span>  <br/> |<span data-ttu-id="2530b-126">EMAIL2 é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="2530b-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="2530b-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2530b-127">0x00000002</span></span>  <br/> |<span data-ttu-id="2530b-128">Email3 é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="2530b-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="2530b-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="2530b-129">0x00000003</span></span>  <br/> |<span data-ttu-id="2530b-130">O fax comercial é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="2530b-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="2530b-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2530b-131">0x00000004</span></span>  <br/> |<span data-ttu-id="2530b-132">O fax residencial é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="2530b-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="2530b-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="2530b-133">0x00000005</span></span>  <br/> |<span data-ttu-id="2530b-134">O fax principal é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="2530b-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2530b-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2530b-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2530b-136">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="2530b-136">Protocol specifications</span></span>

<span data-ttu-id="2530b-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2530b-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2530b-138">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2530b-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2530b-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2530b-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2530b-140">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="2530b-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2530b-141">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2530b-141">Header files</span></span>

<span data-ttu-id="2530b-142">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2530b-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="2530b-143">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2530b-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2530b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="2530b-144">See also</span></span>



[<span data-ttu-id="2530b-145">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2530b-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2530b-146">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2530b-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2530b-147">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2530b-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2530b-148">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2530b-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

