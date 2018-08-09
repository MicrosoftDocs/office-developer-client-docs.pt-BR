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
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768201"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="3607f-103">Propriedade canônica PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="3607f-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="3607f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3607f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3607f-105">Especifica o estado de endereços de eletrônicos do contato e representa um conjunto de sinalizadores de bit.</span><span class="sxs-lookup"><span data-stu-id="3607f-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3607f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3607f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3607f-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="3607f-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="3607f-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="3607f-108">Property set:</span></span>  <br/> |<span data-ttu-id="3607f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3607f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3607f-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="3607f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3607f-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="3607f-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="3607f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3607f-112">Data type:</span></span>  <br/> |<span data-ttu-id="3607f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3607f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3607f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3607f-114">Area:</span></span>  <br/> |<span data-ttu-id="3607f-115">Contato</span><span class="sxs-lookup"><span data-stu-id="3607f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3607f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3607f-116">Remarks</span></span>

<span data-ttu-id="3607f-117">O valor da propriedade **dispidABPArrayType** deve ser uma combinação de sinalizadores que especificam o estado do objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="3607f-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="3607f-118">Sinalizadores individuais são especificados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3607f-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="3607f-119">Se essa propriedade estiver definida, a propriedade **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) deve ser definida, também.</span><span class="sxs-lookup"><span data-stu-id="3607f-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="3607f-120">Essas duas propriedades devem ser mantidas sincronizadas entre si.</span><span class="sxs-lookup"><span data-stu-id="3607f-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="3607f-121">Por exemplo, se **dispidABPArrayType** tiver definido o bit "set 0x00000001", um dos valores de **dispidABPEmailList** deve ser "0x00000000".</span><span class="sxs-lookup"><span data-stu-id="3607f-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="3607f-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="3607f-122">**Bit**</span></span>|<span data-ttu-id="3607f-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3607f-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3607f-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3607f-124">0x00000001</span></span>  <br/> |<span data-ttu-id="3607f-125">Email1 é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="3607f-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="3607f-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3607f-126">0x00000002</span></span>  <br/> |<span data-ttu-id="3607f-127">Email2 é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="3607f-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="3607f-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3607f-128">0x00000004</span></span>  <br/> |<span data-ttu-id="3607f-129">Email3 é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="3607f-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="3607f-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3607f-130">0x00000008</span></span>  <br/> |<span data-ttu-id="3607f-131">Fax comercial é definido para o contato.</span><span class="sxs-lookup"><span data-stu-id="3607f-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="3607f-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3607f-132">0x00000010</span></span>  <br/> |<span data-ttu-id="3607f-133">Fax residencial é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="3607f-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="3607f-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="3607f-134">0x00000020</span></span>  <br/> |<span data-ttu-id="3607f-135">Fax principal é definida para o contato.</span><span class="sxs-lookup"><span data-stu-id="3607f-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3607f-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3607f-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3607f-137">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3607f-137">Protocol specifications</span></span>

<span data-ttu-id="3607f-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3607f-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3607f-139">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3607f-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3607f-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3607f-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3607f-141">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="3607f-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3607f-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3607f-142">Header files</span></span>

<span data-ttu-id="3607f-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3607f-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="3607f-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3607f-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3607f-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="3607f-145">See also</span></span>



[<span data-ttu-id="3607f-146">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3607f-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3607f-147">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3607f-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3607f-148">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3607f-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3607f-149">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3607f-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

