---
title: Propriedade canônica PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316153"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="ba19c-103">Propriedade canônica PidTagGender</span><span class="sxs-lookup"><span data-stu-id="ba19c-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="ba19c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba19c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba19c-105">Contém o sexo do usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ba19c-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba19c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ba19c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba19c-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="ba19c-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="ba19c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ba19c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba19c-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="ba19c-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="ba19c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ba19c-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba19c-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="ba19c-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="ba19c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ba19c-112">Area:</span></span>  <br/> |<span data-ttu-id="ba19c-113">Usuário de email MAPI</span><span class="sxs-lookup"><span data-stu-id="ba19c-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba19c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba19c-114">Remarks</span></span>

<span data-ttu-id="ba19c-115">Esta propriedade fornece informações de identificação e acesso sobre um usuário de mensagens e o conteúdo é.</span><span class="sxs-lookup"><span data-stu-id="ba19c-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="ba19c-116">O conteúdo é definido pelo usuário de mensagens e pela organização do usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ba19c-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="ba19c-117">Os valores possíveis para essa propriedade são definidos na enumeração sexo.</span><span class="sxs-lookup"><span data-stu-id="ba19c-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="ba19c-118">Eles estão listados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ba19c-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="ba19c-119">**Enumeração sexo**</span><span class="sxs-lookup"><span data-stu-id="ba19c-119">**Gender enumeration**</span></span>|<span data-ttu-id="ba19c-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ba19c-120">**Value**</span></span>|<span data-ttu-id="ba19c-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ba19c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba19c-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="ba19c-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="ba19c-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="ba19c-123">0x0000</span></span>  <br/> |<span data-ttu-id="ba19c-124">O sexo do contato não está especificado.</span><span class="sxs-lookup"><span data-stu-id="ba19c-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="ba19c-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="ba19c-125">genderFemale</span></span>  <br/> |<span data-ttu-id="ba19c-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="ba19c-126">0x0001</span></span>  <br/> |<span data-ttu-id="ba19c-127">O contato é fêmea.</span><span class="sxs-lookup"><span data-stu-id="ba19c-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="ba19c-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="ba19c-128">genderMale</span></span>  <br/> |<span data-ttu-id="ba19c-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="ba19c-129">0x0002</span></span>  <br/> |<span data-ttu-id="ba19c-130">O contato é macho.</span><span class="sxs-lookup"><span data-stu-id="ba19c-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ba19c-131">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba19c-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ba19c-132">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="ba19c-132">Protocol specifications</span></span>

<span data-ttu-id="ba19c-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba19c-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba19c-134">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ba19c-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ba19c-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba19c-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba19c-136">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="ba19c-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="ba19c-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ba19c-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ba19c-138">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="ba19c-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ba19c-139">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba19c-139">Header files</span></span>

<span data-ttu-id="ba19c-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ba19c-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba19c-141">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ba19c-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba19c-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ba19c-142">Mapitags.h</span></span>
  
> <span data-ttu-id="ba19c-143">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ba19c-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba19c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba19c-144">See also</span></span>



[<span data-ttu-id="ba19c-145">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ba19c-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba19c-146">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ba19c-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba19c-147">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ba19c-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba19c-148">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ba19c-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

