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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315418"
---
# <a name="pidlidusetnef-canonical-property"></a><span data-ttu-id="8e77e-103">Propriedade canônica PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="8e77e-103">PidLidUseTnef Canonical Property</span></span>

  
  
<span data-ttu-id="8e77e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e77e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e77e-105">Especifica se o formato de encapsulamento de transporte neutro (TNEF) deve ser incluído em uma mensagem quando essa mensagem é convertida de MAPI para Multipurpose Internet Mail Extensions (MIME) ou formato SMTP (Simple Mail Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="8e77e-105">Specifies whether Transport Neutral Encapsulation Format (TNEF) should be included on a message when that message is converted from MAPI to Multipurpose Internet Mail Extensions (MIME) or Simple Mail Transfer Protocol (SMTP) format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e77e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8e77e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e77e-107">dispidUseTNEF</span><span class="sxs-lookup"><span data-stu-id="8e77e-107">dispidUseTNEF</span></span>  <br/> |
|<span data-ttu-id="8e77e-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="8e77e-108">Property set:</span></span>  <br/> |<span data-ttu-id="8e77e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8e77e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8e77e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8e77e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8e77e-111">0x00008582</span><span class="sxs-lookup"><span data-stu-id="8e77e-111">0x00008582</span></span>  <br/> |
|<span data-ttu-id="8e77e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8e77e-112">Data type:</span></span>  <br/> |<span data-ttu-id="8e77e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8e77e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8e77e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8e77e-114">Area:</span></span>  <br/> |<span data-ttu-id="8e77e-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="8e77e-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e77e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e77e-116">Remarks</span></span>

<span data-ttu-id="8e77e-117">Esta propriedade especifica se o TNEF deve ser incluído em uma mensagem quando essa mensagem é convertida de TNEF para o formato MIME ou SMTP.</span><span class="sxs-lookup"><span data-stu-id="8e77e-117">This property specifies whether TNEF should be included on a message when that message is converted from TNEF to MIME or SMTP format.</span></span> <span data-ttu-id="8e77e-118">Essa propriedade pode estar ausente e, em caso afirmativo, o TNEF não deve ser incluído na mensagem.</span><span class="sxs-lookup"><span data-stu-id="8e77e-118">This property may be absent, and if so, TNEF must not be included on the message.</span></span>
  
<span data-ttu-id="8e77e-119">Essa propriedade só se aplica quando a mensagem é enviada de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8e77e-119">This property only applies when the message is sent from a POP3/SMTP mail account and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span>
  
<span data-ttu-id="8e77e-120">Sob determinadas circunstâncias, como quando os botões de votação estão habilitados ou um objeto OLE incorporado é anexado a uma mensagem, o Outlook pode definir essa propriedade para forçar o uso de TNEF.</span><span class="sxs-lookup"><span data-stu-id="8e77e-120">Under certain circumstances, such as when voting buttons are enabled or an OLE embedded object is attached to a message, Outlook can set this property to force the use of TNEF.</span></span>
  
<span data-ttu-id="8e77e-121">A propriedade **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) pode ser usada para impor apenas o texto sem formatação e não o TNEF ao enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="8e77e-121">The **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="8e77e-122">Como o **PidLidUseTNEF** substitui a configuração no **PR_MSG_EDITOR_FORMAT**, um aplicativo que deseja forçar o texto sem formatação em uma mensagem de saída também deve procurar por **PidLidUseTNEF** e redefini-lo como false.</span><span class="sxs-lookup"><span data-stu-id="8e77e-122">Because **PidLidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**, an application that wants to force plain text on an outgoing message should also look for **PidLidUseTNEF** and reset it to FALSE.</span></span> <span data-ttu-id="8e77e-123">Além disso, o suplemento deve remover os recursos de mensagem que exigiram TNEF para evitar anexos inúteis na mensagem que foi enviada por último.</span><span class="sxs-lookup"><span data-stu-id="8e77e-123">Additionally, the add-in must remove the message features that required TNEF to avoid unusable attachments on the message that is finally sent.</span></span> 
  
<span data-ttu-id="8e77e-124">Use o sinalizador **CCSF_USE_TNEF** ao chamar [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem MAPI de saída em um fluxo MIME também pode impor TNEF.</span><span class="sxs-lookup"><span data-stu-id="8e77e-124">Use the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="8e77e-125">Isso se aplica mesmo se **PidLidUseTNEF** não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="8e77e-125">This applies even if **PidLidUseTNEF** is not set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e77e-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e77e-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e77e-127">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="8e77e-127">Protocol specifications</span></span>

<span data-ttu-id="8e77e-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e77e-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e77e-129">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8e77e-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e77e-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e77e-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e77e-131">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8e77e-131">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8e77e-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e77e-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e77e-133">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="8e77e-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e77e-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e77e-134">Header files</span></span>

<span data-ttu-id="8e77e-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8e77e-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e77e-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8e77e-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e77e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e77e-137">See also</span></span>



[<span data-ttu-id="8e77e-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e77e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e77e-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8e77e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e77e-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e77e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e77e-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8e77e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

