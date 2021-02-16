---
title: Propriedade canônica PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348437"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="db82e-103">Propriedade canônica PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="db82e-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="db82e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db82e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db82e-105">Especifica o estado dos endereços eletrônicos do contato e representa um conjunto de sinalizadores de bits.</span><span class="sxs-lookup"><span data-stu-id="db82e-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db82e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="db82e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db82e-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="db82e-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="db82e-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="db82e-108">Property set:</span></span>  <br/> |<span data-ttu-id="db82e-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="db82e-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="db82e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="db82e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="db82e-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="db82e-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="db82e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="db82e-112">Data type:</span></span>  <br/> |<span data-ttu-id="db82e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="db82e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="db82e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="db82e-114">Area:</span></span>  <br/> |<span data-ttu-id="db82e-115">Contato</span><span class="sxs-lookup"><span data-stu-id="db82e-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db82e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="db82e-116">Remarks</span></span>

<span data-ttu-id="db82e-117">O valor da **propriedade dispidABPArrayType** deve ser uma combinação de sinalizadores que especificam o estado do objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="db82e-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="db82e-118">Sinalizadores individuais são especificados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="db82e-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="db82e-119">Se essa propriedade for definida, a **propriedade dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) também deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="db82e-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="db82e-120">Essas duas propriedades devem ser mantidas sincronizadas entre si.</span><span class="sxs-lookup"><span data-stu-id="db82e-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="db82e-121">Por exemplo, se **dispidABPArrayType** tiver o bit "0x00000001 set", um dos valores de **dispidABPEmailList** deverá ser "0x00000000".</span><span class="sxs-lookup"><span data-stu-id="db82e-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="db82e-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="db82e-122">**Bit**</span></span>|<span data-ttu-id="db82e-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="db82e-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db82e-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="db82e-124">0x00000001</span></span>  <br/> |<span data-ttu-id="db82e-125">Email1 é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="db82e-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="db82e-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="db82e-126">0x00000002</span></span>  <br/> |<span data-ttu-id="db82e-127">Email2 é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="db82e-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="db82e-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="db82e-128">0x00000004</span></span>  <br/> |<span data-ttu-id="db82e-129">Email3 é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="db82e-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="db82e-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="db82e-130">0x00000008</span></span>  <br/> |<span data-ttu-id="db82e-131">O fax comercial é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="db82e-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="db82e-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db82e-132">0x00000010</span></span>  <br/> |<span data-ttu-id="db82e-133">O fax home é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="db82e-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="db82e-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="db82e-134">0x00000020</span></span>  <br/> |<span data-ttu-id="db82e-135">O fax principal é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="db82e-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="db82e-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="db82e-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db82e-137">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="db82e-137">Protocol specifications</span></span>

<span data-ttu-id="db82e-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db82e-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db82e-139">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="db82e-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db82e-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db82e-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db82e-141">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="db82e-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db82e-142">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="db82e-142">Header files</span></span>

<span data-ttu-id="db82e-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db82e-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="db82e-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="db82e-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db82e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="db82e-145">See also</span></span>



[<span data-ttu-id="db82e-146">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="db82e-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db82e-147">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="db82e-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db82e-148">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="db82e-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db82e-149">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="db82e-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

