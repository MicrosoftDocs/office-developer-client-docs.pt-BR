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
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431663"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="677c9-103">Propriedade canônica PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="677c9-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="677c9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="677c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="677c9-105">Contém o certificado ASN de um destinatário de mensagem para uso em um relatório.</span><span class="sxs-lookup"><span data-stu-id="677c9-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="677c9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="677c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="677c9-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="677c9-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="677c9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="677c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="677c9-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="677c9-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="677c9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="677c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="677c9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="677c9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="677c9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="677c9-112">Area:</span></span>  <br/> |<span data-ttu-id="677c9-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="677c9-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="677c9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="677c9-114">Remarks</span></span>

<span data-ttu-id="677c9-115">Esta propriedade é uma cópia da propriedade **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) do destinatário para uso em um relatório.</span><span class="sxs-lookup"><span data-stu-id="677c9-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="677c9-116">Ele pode ser usado para provar ao originador de que o destinatário realmente recebeu a mensagem, o que um relatório de entrega não necessariamente indica.</span><span class="sxs-lookup"><span data-stu-id="677c9-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="677c9-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="677c9-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="677c9-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="677c9-118">Header files</span></span>

<span data-ttu-id="677c9-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="677c9-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="677c9-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="677c9-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="677c9-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="677c9-121">Mapitags.h</span></span>
  
> <span data-ttu-id="677c9-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="677c9-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="677c9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="677c9-123">See also</span></span>



[<span data-ttu-id="677c9-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="677c9-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="677c9-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="677c9-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="677c9-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="677c9-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="677c9-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="677c9-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

