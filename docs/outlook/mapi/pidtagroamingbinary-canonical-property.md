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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359560"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="7f390-103">Propriedade canônica PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="7f390-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="7f390-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f390-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f390-105">Contém um fluxo de mensagens associado a uma subclasse de \*\*IPM. \*\*Classe de configuração.</span><span class="sxs-lookup"><span data-stu-id="7f390-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f390-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7f390-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f390-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="7f390-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="7f390-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7f390-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f390-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="7f390-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="7f390-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7f390-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f390-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7f390-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7f390-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7f390-112">Area:</span></span>  <br/> |<span data-ttu-id="7f390-113">Configuração</span><span class="sxs-lookup"><span data-stu-id="7f390-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f390-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f390-114">Remarks</span></span>

<span data-ttu-id="7f390-115">Esta propriedade contém o fluxo de dados associado a um \*\*IPM. \*\*Mensagem de classe da mensagem de configuração.</span><span class="sxs-lookup"><span data-stu-id="7f390-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="7f390-116">O formato do fluxo depende da classe da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7f390-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="7f390-117">Por exemplo, uma mensagem de tipo de classe **IPM. A configuração. AutoComplete** será formatada como um [fluxo de preenchimento automático](autocomplete-stream.md).</span><span class="sxs-lookup"><span data-stu-id="7f390-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f390-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f390-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f390-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="7f390-119">Protocol specifications</span></span>

<span data-ttu-id="7f390-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f390-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f390-121">Fornece referências para as especificações de protocolo do Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7f390-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f390-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f390-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f390-123">Especifica o local e as propriedades dos dados de configuração de cliente e de servidor, como listas de categorias compartilhadas e horários de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7f390-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f390-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7f390-124">Header files</span></span>

<span data-ttu-id="7f390-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f390-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f390-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7f390-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f390-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7f390-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7f390-128">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="7f390-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f390-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f390-129">See also</span></span>



[<span data-ttu-id="7f390-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7f390-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f390-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7f390-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f390-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7f390-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f390-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7f390-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

