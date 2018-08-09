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
ms.openlocfilehash: d27ef47a3ba387ae2e7acbcefc75b07ddd794e80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770157"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="df80e-103">Propriedade canônica PidTagUserX509Certificate</span><span class="sxs-lookup"><span data-stu-id="df80e-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="df80e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df80e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df80e-105">Contém os certificados de segurança x. 509 versão 3 para um usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="df80e-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df80e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="df80e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df80e-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="df80e-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="df80e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="df80e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df80e-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="df80e-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="df80e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="df80e-110">Data type:</span></span>  <br/> |<span data-ttu-id="df80e-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="df80e-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="df80e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="df80e-112">Area:</span></span>  <br/> |<span data-ttu-id="df80e-113">Usuário de email MAPI</span><span class="sxs-lookup"><span data-stu-id="df80e-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df80e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="df80e-114">Remarks</span></span>

<span data-ttu-id="df80e-115">Essa propriedade é usada pelos aplicativos que utilizam a segurança de chave pública.</span><span class="sxs-lookup"><span data-stu-id="df80e-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="df80e-116">Ele contém uma representação binária de um ou mais certificados de segurança 3 de versão de x. 509.</span><span class="sxs-lookup"><span data-stu-id="df80e-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="df80e-117">Vários aplicativos e clientes podem usar essa propriedade para seus próprios certificados de segurança.</span><span class="sxs-lookup"><span data-stu-id="df80e-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="df80e-118">O formato binário dos dados x. 509 pode variar entre os fornecedores.</span><span class="sxs-lookup"><span data-stu-id="df80e-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df80e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="df80e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df80e-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="df80e-120">Protocol specifications</span></span>

<span data-ttu-id="df80e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df80e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df80e-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="df80e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df80e-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df80e-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df80e-124">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="df80e-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df80e-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df80e-125">Header files</span></span>

<span data-ttu-id="df80e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df80e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="df80e-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="df80e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="df80e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df80e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="df80e-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="df80e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df80e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="df80e-130">See also</span></span>



[<span data-ttu-id="df80e-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="df80e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df80e-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="df80e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df80e-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="df80e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df80e-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="df80e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

