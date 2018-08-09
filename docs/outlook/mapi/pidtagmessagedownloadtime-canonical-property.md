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
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769472"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="76357-103">Propriedade canônica PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="76357-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="76357-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76357-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76357-105">Contém o tempo estimado para baixar uma mensagem de um servidor remoto para um armazenamento de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="76357-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76357-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="76357-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76357-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="76357-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="76357-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="76357-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76357-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="76357-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="76357-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="76357-110">Data type:</span></span>  <br/> |<span data-ttu-id="76357-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="76357-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="76357-112">Área:</span><span class="sxs-lookup"><span data-stu-id="76357-112">Area:</span></span>  <br/> |<span data-ttu-id="76357-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="76357-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76357-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="76357-114">Remarks</span></span>

<span data-ttu-id="76357-115">Essa propriedade é expresso em segundos e representa a melhor estimativa de tempo seria necessário um provedor de transporte remoto para baixar uma determinada mensagem de seu local atual para um armazenamento de mensagens local para o cliente de exibição da pasta do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="76357-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="76357-116">Normalmente, o provedor de transporte remoto calcula o valor dessa propriedade dividindo-se o valor da propriedade **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) pela velocidade do link communications em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="76357-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="76357-117">Se o provedor não pode calcular o tempo de download, por exemplo, se não souber a velocidade de link, ele deve fornecer um valor **PT_ERROR** como **MAPI_E_NO_SUPPORT** para esta coluna na tabela de conteúdo de pasta de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="76357-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="76357-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="76357-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="76357-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="76357-119">Header files</span></span>

<span data-ttu-id="76357-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76357-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="76357-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="76357-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="76357-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76357-122">Mapitags.h</span></span>
  
> <span data-ttu-id="76357-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="76357-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76357-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="76357-124">See also</span></span>



[<span data-ttu-id="76357-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="76357-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76357-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="76357-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76357-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="76357-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76357-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="76357-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

