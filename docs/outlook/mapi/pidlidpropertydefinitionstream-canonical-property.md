---
title: Propriedade canônica PidLidPropertyDefinitionStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315936"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="bac68-103">Propriedade canônica PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="bac68-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="bac68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bac68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bac68-105">Representa definições de campos definidos pelo usuário e configurações de vinculação de dados de campos integrados de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bac68-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bac68-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bac68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bac68-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="bac68-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="bac68-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="bac68-108">Property set:</span></span>  <br/> |<span data-ttu-id="bac68-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bac68-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bac68-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bac68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bac68-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="bac68-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="bac68-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bac68-112">Data type:</span></span>  <br/> |<span data-ttu-id="bac68-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bac68-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bac68-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bac68-114">Area:</span></span>  <br/> |<span data-ttu-id="bac68-115">Configuração em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="bac68-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bac68-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bac68-116">Remarks</span></span>

<span data-ttu-id="bac68-117">O valor da **propriedade PidLidPropertyDefinitionStream** é salvo como parte da definição de formulário personalizado para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bac68-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="bac68-118">O valor dessa propriedade é um fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="bac68-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="bac68-119">Para obter informações sobre a estrutura desse fluxo, consulte [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="bac68-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bac68-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bac68-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bac68-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bac68-121">Protocol specifications</span></span>

<span data-ttu-id="bac68-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bac68-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bac68-123">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bac68-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bac68-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="bac68-124">Header files</span></span>

<span data-ttu-id="bac68-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bac68-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bac68-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bac68-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bac68-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="bac68-127">See also</span></span>



[<span data-ttu-id="bac68-128">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="bac68-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="bac68-129">Adicionar uma definição para um novo User-Defined campo</span><span class="sxs-lookup"><span data-stu-id="bac68-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="bac68-130">Exemplo de fluxo propertyDefinition</span><span class="sxs-lookup"><span data-stu-id="bac68-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="bac68-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bac68-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bac68-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bac68-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bac68-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bac68-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bac68-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bac68-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

