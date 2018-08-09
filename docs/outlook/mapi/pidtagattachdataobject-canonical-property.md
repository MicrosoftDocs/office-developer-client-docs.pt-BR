---
title: Propriedade canônica PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3fc7690a8c9eb2ada3a34bc44217ff463721e4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768950"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="9e1a0-103">Propriedade canônica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="9e1a0-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="9e1a0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e1a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e1a0-105">Contém um objeto attachment costumam ser acessado por meio da interface de vinculação e incorporação de objetos (OLE) **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="9e1a0-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e1a0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9e1a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e1a0-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="9e1a0-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="9e1a0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9e1a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e1a0-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="9e1a0-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="9e1a0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9e1a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e1a0-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="9e1a0-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="9e1a0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9e1a0-112">Area:</span></span>  <br/> |<span data-ttu-id="9e1a0-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="9e1a0-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e1a0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e1a0-114">Remarks</span></span>

<span data-ttu-id="9e1a0-115">Essa propriedade contém o anexo, quando o valor da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) é **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="9e1a0-116">O tipo de codificação de OLE pode ser determinado de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e1a0-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="9e1a0-117">Para um anexo associado com o valor **ATTACH_EMBEDDED_MSG** , a interface [IMessage:IMAPIProp](imessageimapiprop.md) pode ser usada para acesso mais rápido.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="9e1a0-118">Para um objeto OLE dinâmico incorporado, a propriedade **PR_ATTACH_DATA_OBJ** contém suas próprias informações de renderização e a propriedade **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) deve ser inexistente ou está vazio.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="9e1a0-119">Para um anexo de arquivo de documento OLE, o provedor de armazenamento de mensagem deve responder a uma chamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em **PR_ATTACH_DATA_OBJ** e, opcionalmente, pode responder a uma chamada em **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="9e1a0-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="9e1a0-120">As propriedades **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** compartilham o mesmo identificador de propriedade e, portanto, são duas representações da mesma propriedade.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="9e1a0-121">Para um objeto de armazenamento, como um arquivo composto no formato de arquivo de documento OLE 2.0, alguns provedores de serviços permitem que ele seja aberto com a interface MAPI **IStreamDocfile** , uma subclasse de **IStream** sem membros adicionais, projetado para otimizar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="9e1a0-122">A economia potencial é suficiente para justificar a tentativa de abrir **PR_ATTACH_DATA_OBJ** por meio de **IStreamDocfile**.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="9e1a0-123">Se **MAPI_E_INTERFACE_NOT_SUPPORTED** for retornado, o cliente pode abrir **PR_ATTACH_DATA_BIN** com **IStream**.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="9e1a0-124">Se o aplicativo cliente ou o provedor de serviço não pode abrir um Subobjeto anexo usando **PR_ATTACH_DATA_OBJ** com a Ajuda de **PR_ATTACH_METHOD**, ele deve usar **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="9e1a0-125">Para obter mais informações sobre formatos e interfaces OLE, consulte [OLE e transferência de dados](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e1a0-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9e1a0-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e1a0-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e1a0-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9e1a0-127">Protocol specifications</span></span>

<span data-ttu-id="9e1a0-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e1a0-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e1a0-129">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="9e1a0-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9e1a0-130">Header Files</span></span>

<span data-ttu-id="9e1a0-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e1a0-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e1a0-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e1a0-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9e1a0-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9e1a0-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9e1a0-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e1a0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e1a0-135">See also</span></span>



[<span data-ttu-id="9e1a0-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9e1a0-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e1a0-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9e1a0-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e1a0-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9e1a0-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e1a0-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9e1a0-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

