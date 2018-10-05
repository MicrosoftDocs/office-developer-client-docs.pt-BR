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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393268"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="4570b-103">Propriedade canônica PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="4570b-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="4570b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4570b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4570b-105">Representa as configurações de associação de dados de campos internos de uma mensagem e definições de campos definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4570b-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4570b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4570b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4570b-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="4570b-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="4570b-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="4570b-108">Property set:</span></span>  <br/> |<span data-ttu-id="4570b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4570b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4570b-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="4570b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4570b-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="4570b-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="4570b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4570b-112">Data type:</span></span>  <br/> |<span data-ttu-id="4570b-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4570b-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4570b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4570b-114">Area:</span></span>  <br/> |<span data-ttu-id="4570b-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="4570b-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4570b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4570b-116">Remarks</span></span>

<span data-ttu-id="4570b-117">O valor da propriedade **PidLidPropertyDefinitionStream** é salvo como parte da definição do formulário personalizado para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4570b-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="4570b-118">O valor dessa propriedade é um fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="4570b-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="4570b-119">Para obter informações sobre a estrutura deste fluxo, consulte [PropertyDefinition Stream estrutura](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="4570b-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4570b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4570b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4570b-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4570b-121">Protocol specifications</span></span>

<span data-ttu-id="4570b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4570b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4570b-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4570b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4570b-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4570b-124">Header files</span></span>

<span data-ttu-id="4570b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4570b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4570b-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4570b-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4570b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4570b-127">See also</span></span>



[<span data-ttu-id="4570b-128">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="4570b-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="4570b-129">Adicionar uma definição de um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="4570b-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="4570b-130">Exemplo de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="4570b-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="4570b-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4570b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4570b-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4570b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4570b-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4570b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4570b-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4570b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

