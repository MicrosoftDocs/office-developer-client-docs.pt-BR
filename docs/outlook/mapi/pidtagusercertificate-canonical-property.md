---
title: Propriedade canônica PidTagUserCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 53ee4019752cf717840199d4a51cbc90133b8636
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393884"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="dcde8-103">Propriedade canônica PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="dcde8-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="dcde8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcde8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcde8-105">Contém um certificado de autenticação de ASN. 1 para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dcde8-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcde8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dcde8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcde8-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="dcde8-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="dcde8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dcde8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dcde8-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="dcde8-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="dcde8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dcde8-110">Data type:</span></span>  <br/> |<span data-ttu-id="dcde8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dcde8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dcde8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dcde8-112">Area:</span></span>  <br/> |<span data-ttu-id="dcde8-113">Usuário de email MAPI</span><span class="sxs-lookup"><span data-stu-id="dcde8-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcde8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcde8-114">Remarks</span></span>

<span data-ttu-id="dcde8-115">Um certificado de autenticação é semelhante a uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="dcde8-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="dcde8-116">Várias propriedades MAPI fornecem certificados ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="dcde8-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dcde8-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcde8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcde8-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="dcde8-118">Protocol specifications</span></span>

<span data-ttu-id="dcde8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcde8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcde8-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dcde8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dcde8-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcde8-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcde8-122">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="dcde8-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcde8-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dcde8-123">Header files</span></span>

<span data-ttu-id="dcde8-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dcde8-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcde8-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dcde8-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="dcde8-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dcde8-126">Mapitags.h</span></span>
  
> <span data-ttu-id="dcde8-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dcde8-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcde8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcde8-128">See also</span></span>



[<span data-ttu-id="dcde8-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dcde8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcde8-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="dcde8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcde8-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dcde8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcde8-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dcde8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

