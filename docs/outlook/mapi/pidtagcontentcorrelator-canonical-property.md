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
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769093"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="c92b2-103">Propriedade canônica PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="c92b2-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="c92b2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c92b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c92b2-105">Contém um valor que o remetente da mensagem pode usar para corresponder a um relatório com a mensagem original.</span><span class="sxs-lookup"><span data-stu-id="c92b2-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c92b2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c92b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c92b2-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="c92b2-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="c92b2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c92b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c92b2-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="c92b2-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="c92b2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c92b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="c92b2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c92b2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c92b2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c92b2-112">Area:</span></span>  <br/> |<span data-ttu-id="c92b2-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="c92b2-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c92b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c92b2-114">Remarks</span></span>

<span data-ttu-id="c92b2-115">O conteúdo da cadeia de caracteres binário é definido pela origem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c92b2-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="c92b2-116">Se o conjunto em uma mensagem de saída, esta propriedade deve ser copiado em todos os relatórios gerados em resposta à mensagem.</span><span class="sxs-lookup"><span data-stu-id="c92b2-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c92b2-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c92b2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c92b2-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c92b2-118">Header files</span></span>

<span data-ttu-id="c92b2-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c92b2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c92b2-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c92b2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c92b2-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c92b2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c92b2-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c92b2-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c92b2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c92b2-123">See also</span></span>



[<span data-ttu-id="c92b2-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c92b2-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c92b2-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c92b2-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c92b2-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c92b2-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c92b2-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c92b2-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

