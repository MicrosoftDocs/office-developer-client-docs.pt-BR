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
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401570"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="13b89-103">Propriedade canônica PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="13b89-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="13b89-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13b89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13b89-105">Especifica o formato para um editor a ser usado para exibir uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="13b89-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13b89-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="13b89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13b89-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="13b89-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="13b89-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="13b89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13b89-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="13b89-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="13b89-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="13b89-110">Data type:</span></span>  <br/> |<span data-ttu-id="13b89-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="13b89-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="13b89-112">Área:</span><span class="sxs-lookup"><span data-stu-id="13b89-112">Area:</span></span>  <br/> |<span data-ttu-id="13b89-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="13b89-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13b89-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="13b89-114">Remarks</span></span>

<span data-ttu-id="13b89-115">Os valores possíveis para **PR_MSG_EDITOR_FORMAT** podem ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="13b89-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="13b89-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="13b89-116">**Value**</span></span>|<span data-ttu-id="13b89-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13b89-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13b89-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="13b89-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="13b89-119">O formato para usar o editor é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="13b89-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="13b89-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="13b89-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="13b89-121">O editor deve exibir a mensagem no formato de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="13b89-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="13b89-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="13b89-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="13b89-123">O editor deve exibir a mensagem no formato HTML.</span><span class="sxs-lookup"><span data-stu-id="13b89-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="13b89-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="13b89-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="13b89-125">O editor deve exibir a mensagem em formato Rich Text.</span><span class="sxs-lookup"><span data-stu-id="13b89-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="13b89-126">Por padrão, email mensagens (com a classe de mensagem **IPM. Observação** ou com uma classe de mensagem personalizada derivada de **IPM. Observe**) enviadas a partir de um email POP3/SMTP conta são enviadas no TNEF Transport Neutral Encapsulation Format ().</span><span class="sxs-lookup"><span data-stu-id="13b89-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="13b89-127">A propriedade **PR_MSG_EDITOR_FORMAT** pode ser usada para impor apenas texto sem formatação e não o TNEF, ao enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="13b89-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="13b89-128">Se **PR_MSG_EDITOR_FORMAT** for definido como **EDITOR_FORMAT_PLAINTEXT**, a mensagem é enviada como texto sem formatação sem TNEF.</span><span class="sxs-lookup"><span data-stu-id="13b89-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="13b89-129">Se **PR_MSG_EDITOR_FORMAT** for definido como **EDITOR_FORMAT_RTF**, a codificação TNEF implicitamente está habilitada e a mensagem é enviada usando o formato de Internet padrão especificado no cliente do Outlook.</span><span class="sxs-lookup"><span data-stu-id="13b89-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="13b89-130">Existem dois outros meios para impor o uso de TNEF ao enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="13b89-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="13b89-131">A definição de **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) denominado propriedade como True em uma mensagem indica o que TNEF deve ser incluído ao converter a mensagem MAPI para MIME/SMTP.</span><span class="sxs-lookup"><span data-stu-id="13b89-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="13b89-132">Observe que **dispidUseTNEF** só se aplica quando a mensagem é enviada a partir de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13b89-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="13b89-133">**dispidUseTNEF** sobrescreve a configuração no **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="13b89-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="13b89-134">Usar o sinalizador **CCSF_USE_TNEF** ao chamar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem de saída de MAPI em um fluxo MIME também pode impor o TNEF.</span><span class="sxs-lookup"><span data-stu-id="13b89-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="13b89-135">Isso se aplica mesmo se **dispidUseTNEF** não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="13b89-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="13b89-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="13b89-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13b89-137">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="13b89-137">Protocol specifications</span></span>

<span data-ttu-id="13b89-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13b89-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13b89-139">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13b89-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13b89-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13b89-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13b89-141">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="13b89-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="13b89-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13b89-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13b89-143">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="13b89-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13b89-144">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="13b89-144">Header files</span></span>

<span data-ttu-id="13b89-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13b89-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="13b89-146">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="13b89-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="13b89-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13b89-147">Mapitags.h</span></span>
  
> <span data-ttu-id="13b89-148">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="13b89-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13b89-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="13b89-149">See also</span></span>



[<span data-ttu-id="13b89-150">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13b89-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13b89-151">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="13b89-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13b89-152">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="13b89-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13b89-153">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="13b89-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

