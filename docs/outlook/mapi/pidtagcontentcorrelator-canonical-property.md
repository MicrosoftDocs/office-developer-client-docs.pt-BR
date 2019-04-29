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
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438523"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="8a127-103">Propriedade canônica PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="8a127-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="8a127-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a127-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a127-105">Contém um valor que o remetente da mensagem pode usar para corresponder a um relatório com a mensagem original.</span><span class="sxs-lookup"><span data-stu-id="8a127-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a127-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8a127-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a127-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="8a127-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="8a127-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8a127-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a127-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="8a127-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="8a127-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8a127-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a127-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a127-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a127-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8a127-112">Area:</span></span>  <br/> |<span data-ttu-id="8a127-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8a127-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a127-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a127-114">Remarks</span></span>

<span data-ttu-id="8a127-115">O conteúdo da cadeia de caracteres binária é definido pelo originador da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a127-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="8a127-116">Se definido em uma mensagem de saída, essa propriedade deve ser copiada em todos os relatórios gerados em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a127-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a127-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a127-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8a127-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8a127-118">Header files</span></span>

<span data-ttu-id="8a127-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8a127-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a127-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8a127-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a127-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8a127-121">Mapitags.h</span></span>
  
> <span data-ttu-id="8a127-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8a127-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a127-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a127-123">See also</span></span>



[<span data-ttu-id="8a127-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8a127-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a127-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8a127-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a127-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8a127-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a127-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8a127-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

