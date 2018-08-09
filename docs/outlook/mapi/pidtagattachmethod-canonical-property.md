---
title: Propriedade canônica PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Modificado pela última vez: 07 de setembro de 2016'
ms.openlocfilehash: 1720e9a2eeb54daed1e559f99b0c63ce09585419
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768988"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="bb381-103">Propriedade canônica PidTagAttachMethod</span><span class="sxs-lookup"><span data-stu-id="bb381-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="bb381-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb381-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb381-105">Contém uma constante definida pelo MAPI que representa a maneira como o conteúdo de um anexo pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="bb381-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb381-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bb381-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb381-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="bb381-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="bb381-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bb381-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb381-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="bb381-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="bb381-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bb381-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb381-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bb381-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bb381-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bb381-112">Area:</span></span>  <br/> |<span data-ttu-id="bb381-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="bb381-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb381-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb381-114">Remarks</span></span>

<span data-ttu-id="bb381-115">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="bb381-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="bb381-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="bb381-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="bb381-117">O anexo foi criado.</span><span class="sxs-lookup"><span data-stu-id="bb381-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="bb381-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="bb381-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="bb381-119">A propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) contém os dados do anexo.</span><span class="sxs-lookup"><span data-stu-id="bb381-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="bb381-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="bb381-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="bb381-121">A propriedade **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) ou **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) contém um caminho totalmente qualificado que identifica o anexo a destinatários com acesso a um arquivo comuns servidor.</span><span class="sxs-lookup"><span data-stu-id="bb381-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="bb381-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="bb381-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="bb381-123">A propriedade **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo.</span><span class="sxs-lookup"><span data-stu-id="bb381-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="bb381-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="bb381-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="bb381-125">A propriedade **PR_ATTACH_PATHNAME** ou **PR_ATTACH_LONG_PATHNAME** contém um caminho totalmente qualificado que identifica o anexo.</span><span class="sxs-lookup"><span data-stu-id="bb381-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="bb381-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="bb381-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="bb381-127">A propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) contém um objeto incorporado que dá suporte à interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="bb381-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="bb381-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="bb381-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="bb381-129">O anexo é um objeto OLE incorporado.</span><span class="sxs-lookup"><span data-stu-id="bb381-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="bb381-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="bb381-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="bb381-131">O conteúdo do anexo não está na mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb381-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="bb381-132">Quando criado, todos os objetos de anexo têm um valor **PR_ATTACH_METHOD** inicial de **NO_ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="bb381-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="bb381-133">Provedores de serviços e aplicativos cliente são necessárias somente para suportar o método de anexo representado pelo valor **ATTACH_BY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="bb381-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="bb381-134">Os outros métodos de anexo são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bb381-134">The other attachment methods are optional.</span></span> <span data-ttu-id="bb381-135">O armazenamento de mensagens não impõe qualquer consistência entre o valor da **PR_ATTACH_METHOD** e os valores das propriedades do anexo.</span><span class="sxs-lookup"><span data-stu-id="bb381-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="bb381-136">Nomes universais de nomenclatura (UNC) da convenção são recomendados para caminhos totalmente qualificado, que devem ser usados com **ATTACH_BY_REFERENCE** e **ATTACH_BY_REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="bb381-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="bb381-137">Com **ATTACH_BY_REF_RESOLVE**, um caminho absoluto é mais rápido, pois o MAPI spooler converte o anexo **ATTACH_BY_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="bb381-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="bb381-138">Se **ATTACH_BY_REFERENCE** estiver definida, **PR_ATTACH_DATA_BIN** deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="bb381-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="bb381-139">Um gateway de saída pode ativar um anexo **ATTACH_BY_REFERENCE** em um anexo **ATTACH_BY_VALUE** , copiando os dados de anexo para a propriedade **PR_ATTACH_DATA_BIN** .</span><span class="sxs-lookup"><span data-stu-id="bb381-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="bb381-140">Se **ATTACH_BY_REF_RESOLVE** estiver definida, **PR_ATTACH_DATA_BIN** deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="bb381-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="bb381-141">Quando a mensagem que contém o anexo **ATTACH_BY_REF_RESOLVE** é enviada, o MAPI spooler copia os dados de anexo em um anexo **ATTACH_BY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="bb381-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="bb381-142">Esse processo de resolução coloca os dados de anexo no **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="bb381-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="bb381-143">Se **ATTACH_BY_REF_ONLY** estiver definida, **PR_ATTACH_DATA_BIN** deve estar vazio e sistema de mensagens nunca resolve a referência de anexo.</span><span class="sxs-lookup"><span data-stu-id="bb381-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="bb381-144">Use esse valor quando você deseja enviar o link, mas não os dados.</span><span class="sxs-lookup"><span data-stu-id="bb381-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="bb381-145">Quando o objeto OLE está no formato OLE 2.0 **IStorage** , os dados são acessíveis através de **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="bb381-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="bb381-146">Quando o objeto OLE está no formato 1.0 OLE **OLESTREAM** , os dados são acessíveis através de **PR_ATTACH_DATA_BIN** como um **IStream**.</span><span class="sxs-lookup"><span data-stu-id="bb381-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="bb381-147">O tipo da codificação OLE pode ser determinado pelo valor **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb381-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="bb381-148">Para obter mais informações sobre formatos e interfaces OLE, consulte a *referência do programador do OLE* .</span><span class="sxs-lookup"><span data-stu-id="bb381-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bb381-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb381-149">Remarks</span></span>

<span data-ttu-id="bb381-150">Quando o **PR_ATTACH_METHOD** for **ATTACH_BY_WEBREFERENCE**, o conteúdo do anexo não está na mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb381-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="bb381-151">Em vez disso, a propriedade **PR_ATTACH_LONG_FILENAME** contém uma URL absoluta para o conteúdo de anexo, que é armazenado online.</span><span class="sxs-lookup"><span data-stu-id="bb381-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bb381-152">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb381-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb381-153">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bb381-153">Protocol specifications</span></span>

<span data-ttu-id="bb381-154">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb381-154">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb381-155">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="bb381-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb381-156">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bb381-156">Header files</span></span>

<span data-ttu-id="bb381-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb381-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb381-158">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bb381-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb381-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bb381-159">Mapitags.h</span></span>
  
> <span data-ttu-id="bb381-160">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bb381-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb381-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb381-161">See also</span></span>



[<span data-ttu-id="bb381-162">Propriedade canônica PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="bb381-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="bb381-163">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bb381-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb381-164">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bb381-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb381-165">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bb381-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb381-166">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bb381-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

