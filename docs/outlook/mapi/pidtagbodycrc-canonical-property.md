---
title: Propriedade canônica PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415177"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="b84a9-103">Propriedade canônica PidTagBodyCrc</span><span class="sxs-lookup"><span data-stu-id="b84a9-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="b84a9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b84a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b84a9-105">Contém um valor CRC (verificação de redundância cíclica) no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b84a9-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b84a9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b84a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b84a9-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="b84a9-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="b84a9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b84a9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b84a9-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="b84a9-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="b84a9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b84a9-110">Data type:</span></span>  <br/> |<span data-ttu-id="b84a9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b84a9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b84a9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b84a9-112">Area:</span></span>  <br/> |<span data-ttu-id="b84a9-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="b84a9-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b84a9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b84a9-114">Remarks</span></span>

<span data-ttu-id="b84a9-115">O armazenamento de mensagens pode usar qualquer algoritmo CRC que gere um PT_LONG valor.</span><span class="sxs-lookup"><span data-stu-id="b84a9-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="b84a9-116">Ele deve calcular essa propriedade como parte do método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) quando a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) tiver sido definida pela primeira vez e sempre que tiver sido modificada subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="b84a9-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="b84a9-117">Um aplicativo cliente usa **PR_BODY_CRC** para auxiliar na comparação de cadeias de caracteres de texto de mensagem contidas **PR_BODY** propriedades ou suas variantes.</span><span class="sxs-lookup"><span data-stu-id="b84a9-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="b84a9-118">Usando essa propriedade, o cliente pode detectar rapidamente e facilmente quando o texto da mensagem foi alterado.</span><span class="sxs-lookup"><span data-stu-id="b84a9-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="b84a9-119">Ele pode obter ganhos significativos de desempenho  usando o **PR_BODY_CRC** em vez de obter PR_BODY do armazenamento de mensagens e compará-lo com uma versão local.</span><span class="sxs-lookup"><span data-stu-id="b84a9-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b84a9-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b84a9-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b84a9-121">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b84a9-121">Header files</span></span>

<span data-ttu-id="b84a9-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b84a9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b84a9-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b84a9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b84a9-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b84a9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b84a9-125">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="b84a9-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b84a9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b84a9-126">See also</span></span>



[<span data-ttu-id="b84a9-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b84a9-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b84a9-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b84a9-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b84a9-129">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b84a9-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b84a9-130">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b84a9-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

