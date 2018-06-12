---
title: Propriedade canônico de PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: dedb60c5356e1dbb6d35f27372a09c152da0fed0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770113"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="0da5e-103">Propriedade canônico de PidTagSwappedToDoData</span><span class="sxs-lookup"><span data-stu-id="0da5e-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="0da5e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0da5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0da5e-105">Mantém um segundo conjunto de valores de propriedade que não afetam o estado sinalizado do objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0da5e-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0da5e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0da5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0da5e-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="0da5e-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="0da5e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0da5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0da5e-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="0da5e-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="0da5e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0da5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0da5e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0da5e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0da5e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0da5e-112">Area:</span></span>  <br/> |<span data-ttu-id="0da5e-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="0da5e-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0da5e-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0da5e-114">Remarks</span></span>

<span data-ttu-id="0da5e-115">Atuando como o local de armazenamento de sinalizador secundário, se houver suporte para sinalizadores de remetente ou lembretes do remetente, esta estrutura oferece um local na qual armazenar todas as propriedades relacionadas ao protocolo de sinalização informativos suportados no sinalizadores de remetente e todos propriedades relacionadas ao protocolo lembrete configurações que são compatíveis com os lembretes de remetente sem expor o sinalizador de remetente ou informações de lembrete do remetente para os destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="0da5e-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="0da5e-116">Da mesma forma, esta estrutura oferece um local na qual armazenar todas as propriedades relacionadas ao protocolo de sinalização informativos suportados no destinatários sinalizadores e propriedades relacionadas ao protocolo lembrete configurações que são compatíveis com o destinatário lembretes em uma mensagem enviada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0da5e-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="0da5e-117">Para obter mais informações sobre essa propriedade, consulte [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0da5e-117">For more information about this property, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0da5e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0da5e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0da5e-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0da5e-119">Protocol specifications</span></span>

<span data-ttu-id="0da5e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0da5e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0da5e-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0da5e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0da5e-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0da5e-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0da5e-123">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="0da5e-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="0da5e-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0da5e-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0da5e-125">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="0da5e-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0da5e-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0da5e-126">Header files</span></span>

<span data-ttu-id="0da5e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0da5e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0da5e-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0da5e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0da5e-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0da5e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0da5e-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0da5e-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0da5e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0da5e-131">See also</span></span>



[<span data-ttu-id="0da5e-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0da5e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0da5e-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0da5e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0da5e-134">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0da5e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0da5e-135">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="0da5e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

