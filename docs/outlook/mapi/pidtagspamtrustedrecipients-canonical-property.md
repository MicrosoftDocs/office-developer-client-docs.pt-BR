---
title: Propriedade canônica PidTagSpamTrustedRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59f43316-3ff6-4ed0-bc29-b31039192b08
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3a852ff8b4e3ff0df59c4c84f53802fa29d63a80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770037"
---
# <a name="pidtagspamtrustedrecipients-canonical-property"></a><span data-ttu-id="2c0f3-103">Propriedade canônica PidTagSpamTrustedRecipients</span><span class="sxs-lookup"><span data-stu-id="2c0f3-103">PidTagSpamTrustedRecipients Canonical Property</span></span>
 
<span data-ttu-id="2c0f3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c0f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c0f3-105">Contém uma lista delimitada por ponto e vírgula dos endereços de email e domínios que representam os destinatários confiáveis.</span><span class="sxs-lookup"><span data-stu-id="2c0f3-105">Contains a semicolon-delimited list of email addresses and domains that represent the trusted recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c0f3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2c0f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c0f3-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span><span class="sxs-lookup"><span data-stu-id="2c0f3-107">PR_SPAM_TRUSTED_RECIPIENTS_W</span></span>  <br/> |
|<span data-ttu-id="2c0f3-108">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="2c0f3-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2c0f3-109">0x0419</span><span class="sxs-lookup"><span data-stu-id="2c0f3-109">0x0419</span></span>  <br/> |
|<span data-ttu-id="2c0f3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2c0f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c0f3-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c0f3-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2c0f3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c0f3-112">Area:</span></span>  <br/> |<span data-ttu-id="2c0f3-113">Spam</span><span class="sxs-lookup"><span data-stu-id="2c0f3-113">Spam</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2c0f3-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c0f3-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c0f3-115">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c0f3-115">Protocol specifications</span></span>

<span data-ttu-id="2c0f3-116">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c0f3-116">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c0f3-117">Fornece referências relacionados especificações de protocolo do Microsoft Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2c0f3-117">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c0f3-118">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c0f3-118">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c0f3-119">Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="2c0f3-119">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c0f3-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c0f3-120">Header files</span></span>

<span data-ttu-id="2c0f3-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c0f3-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c0f3-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2c0f3-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c0f3-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c0f3-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2c0f3-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2c0f3-124">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c0f3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c0f3-125">See also</span></span>

- [<span data-ttu-id="2c0f3-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c0f3-126">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="2c0f3-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2c0f3-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)  
- [<span data-ttu-id="2c0f3-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2c0f3-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)  
- [<span data-ttu-id="2c0f3-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2c0f3-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

