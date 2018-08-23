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
ms.openlocfilehash: 124a0d8f23fcff9d1bca9d5debe4a9aa6fb6146c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587114"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="3e4fc-103">Propriedade canônica PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="3e4fc-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="3e4fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e4fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e4fc-105">Identifica que conta o item de cabeçalho está associado, principalmente para implementar o deixe POP na funcionalidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e4fc-106">Propriedades associadas</span><span class="sxs-lookup"><span data-stu-id="3e4fc-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="3e4fc-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="3e4fc-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="3e4fc-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="3e4fc-108">Property set:</span></span>  <br/> |<span data-ttu-id="3e4fc-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="3e4fc-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="3e4fc-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="3e4fc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3e4fc-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="3e4fc-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="3e4fc-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3e4fc-112">Data type:</span></span>  <br/> |<span data-ttu-id="3e4fc-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3e4fc-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3e4fc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3e4fc-114">Area:</span></span>  <br/> |<span data-ttu-id="3e4fc-115">Mensagem remota</span><span class="sxs-lookup"><span data-stu-id="3e4fc-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e4fc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e4fc-116">Remarks</span></span>

<span data-ttu-id="3e4fc-117">Esta propriedade é relevante somente em mensagens que têm uma classe de mensagem IPM. Remoto.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="3e4fc-118">Microsoft Outlook mantém um mapeamento de várias contas que estiver baixando os dados para um determinado repositório em uma mensagem de informações de associado de pasta (FAI), mas ele também pode manter essas informações no registro.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3e4fc-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e4fc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e4fc-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3e4fc-120">Protocol specifications</span></span>

<span data-ttu-id="3e4fc-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="3e4fc-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3e4fc-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e4fc-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3e4fc-123">Header files</span></span>

<span data-ttu-id="3e4fc-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3e4fc-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e4fc-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e4fc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e4fc-126">See also</span></span>



[<span data-ttu-id="3e4fc-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e4fc-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e4fc-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3e4fc-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e4fc-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3e4fc-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e4fc-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3e4fc-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

