---
title: Propriedade canônica PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382768"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="2c11d-103">Propriedade canônica PidTagAttachEncoding</span><span class="sxs-lookup"><span data-stu-id="2c11d-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="2c11d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c11d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c11d-105">Contém um identificador de objeto ASN. 1 que especifica a codificação de um anexo.</span><span class="sxs-lookup"><span data-stu-id="2c11d-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c11d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2c11d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c11d-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="2c11d-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="2c11d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2c11d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c11d-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="2c11d-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="2c11d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2c11d-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c11d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2c11d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2c11d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c11d-112">Area:</span></span>  <br/> |<span data-ttu-id="2c11d-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="2c11d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c11d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c11d-114">Remarks</span></span>

<span data-ttu-id="2c11d-115">Esta propriedade identifica o algoritmo usado para transformar os dados em um anexo.</span><span class="sxs-lookup"><span data-stu-id="2c11d-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="2c11d-116">**Observação** Não devem ser confundidas os **PR_ATTACH_ENCODING** e as propriedades de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c11d-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="2c11d-117">Eles não são combinados ou relacionados.</span><span class="sxs-lookup"><span data-stu-id="2c11d-117">They are not paired or related.</span></span> <span data-ttu-id="2c11d-118">**PR_ATTACH_TAG** identifica o aplicativo que gerou originalmente o anexo.</span><span class="sxs-lookup"><span data-stu-id="2c11d-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="2c11d-119">"Objeto" tem um significado muito mais geral no identificador de objeto de termos e em x. 400, que na programação orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="2c11d-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="2c11d-120">Identificadores de objeto do objeto identificador sintaxe e exemplo forem definidos no MAPIOID. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="2c11d-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="2c11d-121">Valores para **PR_ATTACH_ENCODING** não estão limitados àqueles definidos no MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="2c11d-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="2c11d-122">Por exemplo, arquivos de Macintosh anexados podem usar um identificador, como MacBinary.</span><span class="sxs-lookup"><span data-stu-id="2c11d-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="2c11d-123">Para obter informações completas sobre esses identificadores de objeto, consulte a documentação sobre ASN. 1, X.208 e 209.</span><span class="sxs-lookup"><span data-stu-id="2c11d-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="2c11d-124">O identificador de objeto é encontrado no elemento de referência do aplicativo do ambiente FTBP (arquivo transferir corpo parte).</span><span class="sxs-lookup"><span data-stu-id="2c11d-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2c11d-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c11d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c11d-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c11d-126">Protocol specifications</span></span>

<span data-ttu-id="2c11d-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c11d-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c11d-128">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="2c11d-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c11d-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c11d-129">Header files</span></span>

<span data-ttu-id="2c11d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c11d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c11d-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2c11d-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c11d-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c11d-132">Mapitags.h</span></span>
  
> <span data-ttu-id="2c11d-133">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2c11d-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c11d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c11d-134">See also</span></span>



[<span data-ttu-id="2c11d-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c11d-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c11d-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2c11d-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c11d-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2c11d-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c11d-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2c11d-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

