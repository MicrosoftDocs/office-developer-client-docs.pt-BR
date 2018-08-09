---
title: Propriedade canônica PidTagRecipientCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769778"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="224a6-103">Propriedade canônica PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="224a6-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="224a6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="224a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="224a6-105">Contém o certificado de ASN. 1 de um destinatário de mensagem para uso em um relatório.</span><span class="sxs-lookup"><span data-stu-id="224a6-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="224a6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="224a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="224a6-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="224a6-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="224a6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="224a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="224a6-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="224a6-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="224a6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="224a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="224a6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="224a6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="224a6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="224a6-112">Area:</span></span>  <br/> |<span data-ttu-id="224a6-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="224a6-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="224a6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="224a6-114">Remarks</span></span>

<span data-ttu-id="224a6-115">Essa propriedade é uma cópia da propriedade de **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) do destinatário para uso em um relatório.</span><span class="sxs-lookup"><span data-stu-id="224a6-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="224a6-116">Ele pode ser usado para provar ao originador que o destinatário realmente recebeu a mensagem, que um relatório de entrega não necessariamente indica.</span><span class="sxs-lookup"><span data-stu-id="224a6-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="224a6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="224a6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="224a6-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="224a6-118">Header files</span></span>

<span data-ttu-id="224a6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="224a6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="224a6-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="224a6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="224a6-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="224a6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="224a6-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="224a6-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="224a6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="224a6-123">See also</span></span>



[<span data-ttu-id="224a6-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="224a6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="224a6-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="224a6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="224a6-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="224a6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="224a6-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="224a6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

