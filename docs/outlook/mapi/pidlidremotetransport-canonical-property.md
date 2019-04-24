---
title: Propriedade canônica PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285176"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="607ad-103">Propriedade canônica PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="607ad-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="607ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="607ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="607ad-105">Identifica a conta à qual o item de cabeçalho está associado, principalmente para implementar a licença POP na funcionalidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="607ad-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="607ad-106">Propriedades associadas</span><span class="sxs-lookup"><span data-stu-id="607ad-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="607ad-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="607ad-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="607ad-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="607ad-108">Property set:</span></span>  <br/> |<span data-ttu-id="607ad-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="607ad-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="607ad-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="607ad-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="607ad-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="607ad-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="607ad-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="607ad-112">Data type:</span></span>  <br/> |<span data-ttu-id="607ad-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="607ad-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="607ad-114">Área:</span><span class="sxs-lookup"><span data-stu-id="607ad-114">Area:</span></span>  <br/> |<span data-ttu-id="607ad-115">Mensagem remota</span><span class="sxs-lookup"><span data-stu-id="607ad-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="607ad-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="607ad-116">Remarks</span></span>

<span data-ttu-id="607ad-117">Esta propriedade é relevante somente em mensagens que têm uma classe de mensagem IPM. Remota.</span><span class="sxs-lookup"><span data-stu-id="607ad-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="607ad-118">O Microsoft Outlook mantém um mapeamento de várias contas que estão sendo baixadas para um determinado repositório em uma mensagem de informações associadas à pasta (FAI), mas também pode manter essas informações no registro.</span><span class="sxs-lookup"><span data-stu-id="607ad-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="607ad-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="607ad-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="607ad-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="607ad-120">Protocol specifications</span></span>

<span data-ttu-id="607ad-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="607ad-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="607ad-122">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="607ad-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="607ad-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="607ad-123">Header files</span></span>

<span data-ttu-id="607ad-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="607ad-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="607ad-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="607ad-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="607ad-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="607ad-126">See also</span></span>



[<span data-ttu-id="607ad-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="607ad-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="607ad-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="607ad-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="607ad-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="607ad-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="607ad-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="607ad-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

