---
title: Propriedade canônica PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6398acf71e62157cf5a6eb7e6caf22130fa9f9d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568802"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="4c3c6-103">Propriedade canônica PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="4c3c6-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="4c3c6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c3c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c3c6-105">Contém um valor que o remetente da mensagem pode usar para corresponder a um relatório com a mensagem original.</span><span class="sxs-lookup"><span data-stu-id="4c3c6-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c3c6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4c3c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c3c6-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="4c3c6-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="4c3c6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4c3c6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c3c6-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="4c3c6-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="4c3c6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4c3c6-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c3c6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4c3c6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4c3c6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4c3c6-112">Area:</span></span>  <br/> |<span data-ttu-id="4c3c6-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="4c3c6-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c3c6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c3c6-114">Remarks</span></span>

<span data-ttu-id="4c3c6-115">O conteúdo da cadeia de caracteres binário é definido pela origem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c3c6-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="4c3c6-116">Se o conjunto em uma mensagem de saída, esta propriedade deve ser copiado em todos os relatórios gerados em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c3c6-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c3c6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c3c6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4c3c6-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4c3c6-118">Header files</span></span>

<span data-ttu-id="4c3c6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c3c6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c3c6-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4c3c6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c3c6-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c3c6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4c3c6-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="4c3c6-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c3c6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c3c6-123">See also</span></span>



[<span data-ttu-id="4c3c6-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4c3c6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c3c6-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4c3c6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c3c6-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4c3c6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c3c6-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4c3c6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

