---
title: Propriedade canônica PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356543"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="48393-103">Propriedade canônica PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="48393-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="48393-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48393-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48393-105">Contém dados de anexo binários normalmente acessados por meio da interface de vinculação e incorporação de objetos (OLE) **IStream** .</span><span class="sxs-lookup"><span data-stu-id="48393-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48393-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="48393-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48393-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="48393-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="48393-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="48393-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48393-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="48393-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="48393-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="48393-110">Data type:</span></span>  <br/> |<span data-ttu-id="48393-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="48393-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="48393-112">Área:</span><span class="sxs-lookup"><span data-stu-id="48393-112">Area:</span></span>  <br/> |<span data-ttu-id="48393-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="48393-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48393-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="48393-114">Remarks</span></span>

<span data-ttu-id="48393-115">Essa propriedade contém o anexo quando o valor da propriedade **PR_ATTACH_METHOD** ([PIDTAGATTACHMETHOD](pidtagattachmethod-canonical-property.md)) é ATTACH_BY_VALUE, que é o método de anexo usual e o único necessário para ter suporte.</span><span class="sxs-lookup"><span data-stu-id="48393-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="48393-116">**PR_ATTACH_DATA_BIN** também mantém um anexo de **OLESTREAM** OLE 1,0 quando o valor de **PR_ATTACH_METHOD** for ATTACH_OLE.</span><span class="sxs-lookup"><span data-stu-id="48393-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="48393-117">Os anexos de **OLESTREAM** podem ser copiados em um arquivo chamando o método OLE **IStream:: CopyTo** .</span><span class="sxs-lookup"><span data-stu-id="48393-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="48393-118">O tipo de codificação OLE pode ser determinado a partir da propriedade **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48393-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="48393-119">Para um anexo de arquivo de documento OLE, o provedor do repositório de mensagens deve responder a uma chamada de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) no **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) e, opcionalmente, responder a uma chamada no \*\*PR_ATTACH_DATA_BIN \*\*.</span><span class="sxs-lookup"><span data-stu-id="48393-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="48393-120">Observe que **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** compartilham o mesmo identificador de propriedade e, portanto, são duas rendições da mesma propriedade.</span><span class="sxs-lookup"><span data-stu-id="48393-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="48393-121">Para um objeto de armazenamento, como um arquivo composto no formato de DOCFILE OLE 2,0, alguns provedores de serviços permitem que ele seja aberto com a interface MAPI **IStreamDocfile** para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="48393-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="48393-122">Um provedor que dá suporte a **IStreamDocfile** deve expô-lo no **PR_ATTACH_DATA_OBJ** e pode, opcionalmente, expô-lo em **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="48393-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="48393-123">Para obter mais informações sobre interfaces e formatos OLE, consulte [OLE e transferência de dados](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="48393-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48393-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="48393-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48393-125">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="48393-125">Protocol specifications</span></span>

<span data-ttu-id="48393-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48393-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48393-127">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="48393-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="48393-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="48393-128">Header Files</span></span>

<span data-ttu-id="48393-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="48393-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="48393-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="48393-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="48393-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="48393-131">Mapitags.h</span></span>
  
> <span data-ttu-id="48393-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="48393-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48393-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="48393-133">See also</span></span>



[<span data-ttu-id="48393-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="48393-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48393-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="48393-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48393-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="48393-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48393-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="48393-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

