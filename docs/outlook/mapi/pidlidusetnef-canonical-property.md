---
title: Propriedade canônica PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384974"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="ef155-103">Propriedade canônica PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="ef155-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="ef155-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef155-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef155-105">Especifica se o TNEF Transport Neutral Encapsulation Format () deve ser incluído em uma mensagem quando a mensagem é convertida de MAPI para o formato do Multipurpose Internet Mail Extensions (MIME) ou Simple Mail Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="ef155-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef155-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ef155-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef155-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="ef155-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="ef155-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="ef155-108">Property set:</span></span>  <br/> |<span data-ttu-id="ef155-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ef155-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ef155-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="ef155-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ef155-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="ef155-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="ef155-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ef155-112">Data type:</span></span>  <br/> |<span data-ttu-id="ef155-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ef155-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ef155-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ef155-114">Area:</span></span>  <br/> |<span data-ttu-id="ef155-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="ef155-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef155-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef155-116">Remarks</span></span>

<span data-ttu-id="ef155-117">Esta propriedade especifica se o TNEF deve ser incluído em uma mensagem quando a mensagem é convertida de TNEF para o formato MIME ou SMTP.</span><span class="sxs-lookup"><span data-stu-id="ef155-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="ef155-118">Essa propriedade pode ser ausente e, em caso afirmativo, TNEF não deve ser incluído na mensagem.</span><span class="sxs-lookup"><span data-stu-id="ef155-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="ef155-119">Essa propriedade só se aplica quando a mensagem é enviada a partir de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef155-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="ef155-120">Sob determinadas circunstâncias, como quando votação botões estão ativados ou uma OLE incorporado o objeto é anexado a uma mensagem, o Outlook pode definir essa propriedade para forçar o uso do TNEF.</span><span class="sxs-lookup"><span data-stu-id="ef155-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="ef155-121">A propriedade **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) pode ser usada para impor apenas texto sem formatação e não o TNEF, ao enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ef155-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="ef155-122">Porque **PidLidUseTNEF** substitui a configuração em **PR_MSG_EDITOR_FORMAT**, um aplicativo que deseja forçar o texto sem formatação em uma mensagem de saída também deve procurar **PidLidUseTNEF** e redefini-lo como FALSE.</span><span class="sxs-lookup"><span data-stu-id="ef155-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="ef155-123">Além disso, o suplemento deve remover os recursos de mensagem que exigiam o TNEF evitar anexos não utilizável na mensagem que é enviada por último.</span><span class="sxs-lookup"><span data-stu-id="ef155-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="ef155-124">Use o sinalizador **CCSF_USE_TNEF** ao chamar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem de MAPI de saída para um fluxo MIME também pode impor TNEF.</span><span class="sxs-lookup"><span data-stu-id="ef155-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="ef155-125">Isso se aplica mesmo se **PidLidUseTNEF** não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="ef155-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ef155-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef155-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef155-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ef155-127">Protocol specifications</span></span>

<span data-ttu-id="ef155-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef155-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef155-129">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ef155-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef155-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef155-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef155-131">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="ef155-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ef155-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef155-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef155-133">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="ef155-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef155-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ef155-134">Header files</span></span>

<span data-ttu-id="ef155-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef155-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef155-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ef155-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef155-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef155-137">See also</span></span>



[<span data-ttu-id="ef155-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ef155-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef155-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ef155-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef155-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ef155-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef155-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ef155-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

