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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356711"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="183ef-103">Propriedade canônica PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="183ef-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="183ef-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="183ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="183ef-105">Contém o certificado ASN de um destinatário de mensagem para uso em um relatório.</span><span class="sxs-lookup"><span data-stu-id="183ef-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="183ef-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="183ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="183ef-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="183ef-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="183ef-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="183ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="183ef-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="183ef-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="183ef-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="183ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="183ef-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="183ef-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="183ef-112">Área:</span><span class="sxs-lookup"><span data-stu-id="183ef-112">Area:</span></span>  <br/> |<span data-ttu-id="183ef-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="183ef-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="183ef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="183ef-114">Remarks</span></span>

<span data-ttu-id="183ef-115">Esta propriedade é uma cópia da propriedade **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) do destinatário para uso em um relatório.</span><span class="sxs-lookup"><span data-stu-id="183ef-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="183ef-116">Ele pode ser usado para provar ao originador de que o destinatário realmente recebeu a mensagem, o que um relatório de entrega não necessariamente indica.</span><span class="sxs-lookup"><span data-stu-id="183ef-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="183ef-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="183ef-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="183ef-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="183ef-118">Header files</span></span>

<span data-ttu-id="183ef-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="183ef-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="183ef-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="183ef-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="183ef-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="183ef-121">Mapitags.h</span></span>
  
> <span data-ttu-id="183ef-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="183ef-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="183ef-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="183ef-123">See also</span></span>



[<span data-ttu-id="183ef-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="183ef-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="183ef-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="183ef-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="183ef-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="183ef-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="183ef-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="183ef-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

