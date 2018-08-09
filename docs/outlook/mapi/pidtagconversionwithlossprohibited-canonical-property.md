---
title: Propriedade canônica PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eee70d97c35c7f115e424905b9e36f3dfa392c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769146"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="82b09-103">Propriedade canônica PidTagConversionWithLossProhibited</span><span class="sxs-lookup"><span data-stu-id="82b09-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="82b09-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82b09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82b09-105">Conterá TRUE se um agente de transferência de mensagem (MTA) é proibido de fazerem conversões de texto que perdem informações de mensagem.</span><span class="sxs-lookup"><span data-stu-id="82b09-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82b09-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="82b09-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82b09-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="82b09-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="82b09-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="82b09-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82b09-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="82b09-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="82b09-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="82b09-110">Data type:</span></span>  <br/> |<span data-ttu-id="82b09-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="82b09-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="82b09-112">Área:</span><span class="sxs-lookup"><span data-stu-id="82b09-112">Area:</span></span>  <br/> |<span data-ttu-id="82b09-113">Configuração geral</span><span class="sxs-lookup"><span data-stu-id="82b09-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82b09-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="82b09-114">Remarks</span></span>

<span data-ttu-id="82b09-115">Um exemplo do tipo de conversão que está sendo proibida é o mapeamento "com perdas" do Unicode (dois bytes por caractere) para um conjunto de caracteres de byte único.</span><span class="sxs-lookup"><span data-stu-id="82b09-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="82b09-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="82b09-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="82b09-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82b09-117">Header files</span></span>

<span data-ttu-id="82b09-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82b09-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="82b09-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="82b09-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="82b09-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82b09-120">Mapitags.h</span></span>
  
> <span data-ttu-id="82b09-121">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="82b09-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82b09-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="82b09-122">See also</span></span>



[<span data-ttu-id="82b09-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="82b09-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82b09-124">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="82b09-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82b09-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="82b09-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82b09-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="82b09-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

