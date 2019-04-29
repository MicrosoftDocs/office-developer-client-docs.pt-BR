---
title: Propriedade canônica PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407925"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="e3856-103">Propriedade canônica PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="e3856-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="e3856-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3856-105">Contém o tempo estimado para baixar uma mensagem de um servidor remoto para um repositório de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="e3856-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3856-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e3856-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3856-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="e3856-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="e3856-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e3856-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3856-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="e3856-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="e3856-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e3856-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3856-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e3856-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e3856-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e3856-112">Area:</span></span>  <br/> |<span data-ttu-id="e3856-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="e3856-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3856-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3856-114">Remarks</span></span>

<span data-ttu-id="e3856-115">Essa propriedade é expressa em segundos e representa a melhor estimativa do tempo que levaria um provedor de transporte remoto para baixar uma determinada mensagem de seu local atual para um repositório de mensagens local para o cliente exibindo a pasta de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="e3856-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="e3856-116">O provedor de transporte remoto normalmente calcula o valor dessa propriedade dividindo o valor da propriedade **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) pela velocidade do link de comunicação em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="e3856-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="e3856-117">Se o provedor não puder calcular o tempo de download, por exemplo, se não souber a velocidade do link, ele deverá fornecer um valor **PT_ERROR** como **MAPI_E_NO_SUPPORT** para esta coluna na tabela de conteúdo da pasta de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="e3856-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e3856-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3856-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e3856-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e3856-119">Header files</span></span>

<span data-ttu-id="e3856-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e3856-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3856-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e3856-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3856-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e3856-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e3856-123">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e3856-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3856-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3856-124">See also</span></span>



[<span data-ttu-id="e3856-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e3856-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3856-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e3856-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3856-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e3856-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3856-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e3856-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

