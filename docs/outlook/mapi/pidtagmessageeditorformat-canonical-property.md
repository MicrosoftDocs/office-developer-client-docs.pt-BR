---
title: Propriedade canônica PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c9c12d3e8314dea5be67727d0f286e7df13038fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574367"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="cf645-103">Propriedade canônica PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="cf645-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="cf645-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf645-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf645-105">Especifica o formato para um editor a ser usado para exibir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf645-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf645-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cf645-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf645-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="cf645-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="cf645-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cf645-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf645-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="cf645-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="cf645-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cf645-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf645-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cf645-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cf645-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cf645-112">Area:</span></span>  <br/> |<span data-ttu-id="cf645-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="cf645-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf645-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf645-114">Remarks</span></span>

<span data-ttu-id="cf645-115">Os valores possíveis para **PR_MSG_EDITOR_FORMAT** podem ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="cf645-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="cf645-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cf645-116">**Value**</span></span>|<span data-ttu-id="cf645-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cf645-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf645-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="cf645-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="cf645-119">O formato para usar o editor é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="cf645-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="cf645-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="cf645-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="cf645-121">O editor deve exibir a mensagem no formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="cf645-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="cf645-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="cf645-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="cf645-123">O editor deve exibir a mensagem no formato HTML.</span><span class="sxs-lookup"><span data-stu-id="cf645-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="cf645-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="cf645-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="cf645-125">O editor deve exibir a mensagem em formato Rich Text.</span><span class="sxs-lookup"><span data-stu-id="cf645-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="cf645-126">Por padrão, email mensagens (com a classe de mensagem **IPM. Observação** ou com uma classe de mensagem personalizada derivada de **IPM. Observe**) enviadas a partir de um email POP3/SMTP conta são enviadas no TNEF Transport Neutral Encapsulation Format ().</span><span class="sxs-lookup"><span data-stu-id="cf645-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="cf645-127">A propriedade **PR_MSG_EDITOR_FORMAT** pode ser usada para impor apenas texto sem formatação e não o TNEF, ao enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf645-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="cf645-128">Se **PR_MSG_EDITOR_FORMAT** for definido como **EDITOR_FORMAT_PLAINTEXT**, a mensagem é enviada como texto sem formatação sem TNEF.</span><span class="sxs-lookup"><span data-stu-id="cf645-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="cf645-129">Se **PR_MSG_EDITOR_FORMAT** for definido como **EDITOR_FORMAT_RTF**, a codificação TNEF implicitamente está habilitada e a mensagem é enviada usando o formato de Internet padrão especificado no cliente do Outlook.</span><span class="sxs-lookup"><span data-stu-id="cf645-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="cf645-130">Existem dois outros meios para impor o uso de TNEF ao enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf645-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="cf645-131">A definição de **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) denominado propriedade como True em uma mensagem indica o que TNEF deve ser incluído ao converter a mensagem MAPI para MIME/SMTP.</span><span class="sxs-lookup"><span data-stu-id="cf645-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="cf645-132">Observe que **dispidUseTNEF** só se aplica quando a mensagem é enviada a partir de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cf645-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="cf645-133">**dispidUseTNEF** sobrescreve a configuração no **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="cf645-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="cf645-134">Usar o sinalizador **CCSF_USE_TNEF** ao chamar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem de saída de MAPI em um fluxo MIME também pode impor o TNEF.</span><span class="sxs-lookup"><span data-stu-id="cf645-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="cf645-135">Isso se aplica mesmo se **dispidUseTNEF** não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="cf645-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="cf645-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf645-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf645-137">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cf645-137">Protocol specifications</span></span>

<span data-ttu-id="cf645-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf645-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf645-139">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cf645-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf645-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf645-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf645-141">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="cf645-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="cf645-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf645-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf645-143">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="cf645-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf645-144">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf645-144">Header files</span></span>

<span data-ttu-id="cf645-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf645-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf645-146">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cf645-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf645-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cf645-147">Mapitags.h</span></span>
  
> <span data-ttu-id="cf645-148">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cf645-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf645-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf645-149">See also</span></span>



[<span data-ttu-id="cf645-150">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cf645-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf645-151">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cf645-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf645-152">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cf645-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf645-153">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cf645-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

