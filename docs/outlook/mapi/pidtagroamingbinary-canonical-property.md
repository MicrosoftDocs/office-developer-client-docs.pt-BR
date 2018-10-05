---
title: Propriedade canônica PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401668"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="d846c-103">Propriedade canônica PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="d846c-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="d846c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d846c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d846c-105">Contém um fluxo de mensagens associado a uma subclasse do **IPM. Configuração** classe.</span><span class="sxs-lookup"><span data-stu-id="d846c-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d846c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d846c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d846c-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="d846c-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="d846c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d846c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d846c-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="d846c-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="d846c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d846c-110">Data type:</span></span>  <br/> |<span data-ttu-id="d846c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d846c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d846c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d846c-112">Area:</span></span>  <br/> |<span data-ttu-id="d846c-113">Configuração</span><span class="sxs-lookup"><span data-stu-id="d846c-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d846c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d846c-114">Remarks</span></span>

<span data-ttu-id="d846c-115">Essa propriedade contém o fluxo de dados associado a um **IPM. Configuração** mensagem de classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d846c-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="d846c-116">O formato do fluxo depende de classe da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d846c-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="d846c-117">Por exemplo, uma mensagem do tipo de classe **IPM. Configuration.Autocomplete** seria formatada como um [fluxo de AutoCompletar](autocomplete-stream.md).</span><span class="sxs-lookup"><span data-stu-id="d846c-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d846c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d846c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d846c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d846c-119">Protocol specifications</span></span>

<span data-ttu-id="d846c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d846c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d846c-121">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d846c-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d846c-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d846c-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d846c-123">Especifica o local e as propriedades de dados de configuração de cliente e servidor, como listas de categoria compartilhada e o horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d846c-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d846c-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d846c-124">Header files</span></span>

<span data-ttu-id="d846c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d846c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d846c-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d846c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d846c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d846c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d846c-128">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="d846c-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d846c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d846c-129">See also</span></span>



[<span data-ttu-id="d846c-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d846c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d846c-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d846c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d846c-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d846c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d846c-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d846c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

