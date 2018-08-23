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
ms.openlocfilehash: 23850e7da71125642abd8484fb45b8ec23264748
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587646"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="75a01-103">Propriedade canônica PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="75a01-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="75a01-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75a01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75a01-105">Representa as configurações de associação de dados de campos internos de uma mensagem e definições de campos definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="75a01-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75a01-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="75a01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75a01-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="75a01-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="75a01-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="75a01-108">Property set:</span></span>  <br/> |<span data-ttu-id="75a01-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="75a01-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="75a01-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="75a01-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="75a01-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="75a01-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="75a01-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="75a01-112">Data type:</span></span>  <br/> |<span data-ttu-id="75a01-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="75a01-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="75a01-114">Área:</span><span class="sxs-lookup"><span data-stu-id="75a01-114">Area:</span></span>  <br/> |<span data-ttu-id="75a01-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="75a01-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75a01-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="75a01-116">Remarks</span></span>

<span data-ttu-id="75a01-117">O valor da propriedade **PidLidPropertyDefinitionStream** é salvo como parte da definição do formulário personalizado para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="75a01-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="75a01-118">O valor dessa propriedade é um fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="75a01-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="75a01-119">Para obter informações sobre a estrutura deste fluxo, consulte [PropertyDefinition Stream estrutura](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="75a01-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75a01-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="75a01-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75a01-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="75a01-121">Protocol specifications</span></span>

<span data-ttu-id="75a01-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a01-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a01-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="75a01-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75a01-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="75a01-124">Header files</span></span>

<span data-ttu-id="75a01-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75a01-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="75a01-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="75a01-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75a01-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="75a01-127">See also</span></span>



[<span data-ttu-id="75a01-128">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="75a01-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="75a01-129">Adicionar uma definição de um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="75a01-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="75a01-130">Exemplo de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="75a01-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="75a01-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="75a01-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75a01-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="75a01-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75a01-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="75a01-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75a01-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="75a01-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

