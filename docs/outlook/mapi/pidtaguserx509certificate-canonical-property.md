---
title: Propriedade canônica PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360715"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="bcf8b-103">Propriedade canônica PidTagUserX509Certificate</span><span class="sxs-lookup"><span data-stu-id="bcf8b-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="bcf8b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcf8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcf8b-105">Contém certificados de segurança X.509 versão 3 para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcf8b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bcf8b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcf8b-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="bcf8b-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="bcf8b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bcf8b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcf8b-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="bcf8b-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="bcf8b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bcf8b-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcf8b-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bcf8b-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="bcf8b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bcf8b-112">Area:</span></span>  <br/> |<span data-ttu-id="bcf8b-113">Usuário de email MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf8b-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcf8b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcf8b-114">Remarks</span></span>

<span data-ttu-id="bcf8b-115">Essa propriedade é usada por aplicativos que utilizam a segurança de chave pública.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="bcf8b-116">Ele contém uma representação binária de um ou mais certificados de segurança X.509 versão 3.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="bcf8b-117">Vários aplicativos e clientes podem usar essa propriedade para seus próprios certificados de segurança.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="bcf8b-118">O formato binário dos dados X.509 pode variar entre os fornecedores.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bcf8b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcf8b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcf8b-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bcf8b-120">Protocol specifications</span></span>

<span data-ttu-id="bcf8b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcf8b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcf8b-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcf8b-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcf8b-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcf8b-124">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcf8b-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="bcf8b-125">Header files</span></span>

<span data-ttu-id="bcf8b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcf8b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcf8b-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcf8b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bcf8b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bcf8b-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bcf8b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcf8b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcf8b-130">See also</span></span>



[<span data-ttu-id="bcf8b-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf8b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcf8b-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf8b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcf8b-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bcf8b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcf8b-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bcf8b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

