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
ms.openlocfilehash: 0863973a420920189cc32324154f1125a2b068fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569943"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="cb409-103">Propriedade canônica PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="cb409-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="cb409-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb409-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb409-105">Contém um certificado de autenticação de ASN. 1 para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cb409-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb409-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cb409-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb409-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="cb409-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="cb409-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb409-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb409-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="cb409-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="cb409-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cb409-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb409-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb409-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cb409-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cb409-112">Area:</span></span>  <br/> |<span data-ttu-id="cb409-113">Usuário de email MAPI</span><span class="sxs-lookup"><span data-stu-id="cb409-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb409-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb409-114">Remarks</span></span>

<span data-ttu-id="cb409-115">Um certificado de autenticação é semelhante a uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="cb409-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="cb409-116">Várias propriedades MAPI fornecem certificados ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="cb409-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cb409-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb409-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb409-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb409-118">Protocol specifications</span></span>

<span data-ttu-id="cb409-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb409-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb409-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cb409-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb409-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb409-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb409-122">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="cb409-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb409-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cb409-123">Header files</span></span>

<span data-ttu-id="cb409-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb409-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb409-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cb409-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb409-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cb409-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cb409-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cb409-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb409-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb409-128">See also</span></span>



[<span data-ttu-id="cb409-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb409-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb409-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cb409-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb409-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cb409-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb409-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cb409-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

