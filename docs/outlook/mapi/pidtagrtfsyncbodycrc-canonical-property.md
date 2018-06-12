---
title: Propriedade canônico de PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: aa144ca93e8fad9b9b5a5da1ee457e5cc3bbd841
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769890"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="61c6f-103">Propriedade canônico de PidTagRtfSyncBodyCrc</span><span class="sxs-lookup"><span data-stu-id="61c6f-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="61c6f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61c6f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61c6f-105">Contém a verificação de redundância cíclica (CRC) computada para o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="61c6f-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61c6f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="61c6f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61c6f-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="61c6f-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="61c6f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="61c6f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61c6f-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="61c6f-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="61c6f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="61c6f-110">Data type:</span></span>  <br/> |<span data-ttu-id="61c6f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="61c6f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="61c6f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="61c6f-112">Area:</span></span>  <br/> |<span data-ttu-id="61c6f-113">Mensagem MAPI</span><span class="sxs-lookup"><span data-stu-id="61c6f-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61c6f-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="61c6f-114">Remarks</span></span>

<span data-ttu-id="61c6f-115">A função [RTFSync](rtfsync.md) computa o CRC usando somente os caracteres que ele considera como significativo à mensagem.</span><span class="sxs-lookup"><span data-stu-id="61c6f-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="61c6f-116">Por exemplo, alguns espaços em branco e outros caracteres ignorável tenham sido omitidos o CRC.</span><span class="sxs-lookup"><span data-stu-id="61c6f-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="61c6f-117">Essa propriedade é uma propriedade de auxiliar formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="61c6f-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="61c6f-118">Essas propriedades são usadas pela função **RTFSync** e não se destina a ser usado diretamente por aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="61c6f-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="61c6f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="61c6f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61c6f-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="61c6f-120">Protocol specifications</span></span>

<span data-ttu-id="61c6f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61c6f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61c6f-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="61c6f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61c6f-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61c6f-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61c6f-124">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="61c6f-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="61c6f-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61c6f-125">Header files</span></span>

<span data-ttu-id="61c6f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61c6f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="61c6f-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="61c6f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="61c6f-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="61c6f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="61c6f-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="61c6f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61c6f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="61c6f-130">See also</span></span>



[<span data-ttu-id="61c6f-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="61c6f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61c6f-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="61c6f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61c6f-133">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="61c6f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61c6f-134">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="61c6f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

