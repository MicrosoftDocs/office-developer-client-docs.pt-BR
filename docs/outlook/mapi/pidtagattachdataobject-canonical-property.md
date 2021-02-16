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
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339281"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="1ca2e-103">Propriedade canônica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="1ca2e-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="1ca2e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ca2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ca2e-105">Contém um objeto attachment normalmente acessado por meio da interface **IStorage** OLE (Object Linking and Embedding).</span><span class="sxs-lookup"><span data-stu-id="1ca2e-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ca2e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1ca2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ca2e-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="1ca2e-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="1ca2e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1ca2e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ca2e-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="1ca2e-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="1ca2e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1ca2e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ca2e-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="1ca2e-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="1ca2e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1ca2e-112">Area:</span></span>  <br/> |<span data-ttu-id="1ca2e-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="1ca2e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ca2e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ca2e-114">Remarks</span></span>

<span data-ttu-id="1ca2e-115">Essa propriedade retém o anexo quando o valor da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) é **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="1ca2e-116">O tipo de codificação OLE pode ser determinado PR_ATTACH_TAG **(** [PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1ca2e-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="1ca2e-117">Para um anexo associado ao valor **ATTACH_EMBEDDED_MSG,** a interface [IMessage:IMAPIProp](imessageimapiprop.md) pode ser usada para acesso mais rápido.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="1ca2e-118">Para um objeto OLE dinâmico incorporado, **a** propriedade PR_ATTACH_DATA_OBJ contém suas próprias informações de renderização e a propriedade **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) deve ser inexistente ou vazio.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="1ca2e-119">Para um anexo de arquivo de documento OLE, o provedor de armazenamento de mensagens deve responder a uma chamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) no **PR_ATTACH_DATA_OBJ** e, opcionalmente, pode responder a uma chamada no **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1ca2e-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="1ca2e-120">As **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** propriedades compartilham o mesmo identificador de propriedade e, portanto, são duas representações da mesma propriedade.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="1ca2e-121">Para um objeto de armazenamento, como um arquivo composto no formato docfile OLE 2.0, alguns provedores de serviços permitem que ele seja aberto com a interface **IStreamDocfile** MAPI, uma subclasse **de IStream** sem membros adicionais, projetada para otimizar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="1ca2e-122">O possível salvar é suficiente para justificar a tentativa de abrir **PR_ATTACH_DATA_OBJ** por **meio de IStreamDocfile**.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="1ca2e-123">Se **MAPI_E_INTERFACE_NOT_SUPPORTED** for retornado, o cliente poderá **abri-PR_ATTACH_DATA_BIN** com **IStream.**</span><span class="sxs-lookup"><span data-stu-id="1ca2e-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="1ca2e-124">Se o aplicativo cliente ou o provedor de serviços não puder abrir um subobjeto de anexo usando o **PR_ATTACH_DATA_OBJ** com a ajuda do **PR_ATTACH_METHOD**, ele deverá **usar** PR_ATTACH_DATA_BIN .</span><span class="sxs-lookup"><span data-stu-id="1ca2e-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="1ca2e-125">Para obter mais informações sobre interfaces e formatos OLE, consulte [OLE e Transferência de Dados.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ca2e-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1ca2e-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ca2e-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ca2e-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1ca2e-127">Protocol specifications</span></span>

<span data-ttu-id="1ca2e-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ca2e-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ca2e-129">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="1ca2e-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1ca2e-130">Header Files</span></span>

<span data-ttu-id="1ca2e-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ca2e-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ca2e-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ca2e-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1ca2e-133">Mapitags.h</span></span>
  
> <span data-ttu-id="1ca2e-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1ca2e-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ca2e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ca2e-135">See also</span></span>



[<span data-ttu-id="1ca2e-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1ca2e-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ca2e-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ca2e-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ca2e-138">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1ca2e-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ca2e-139">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1ca2e-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

