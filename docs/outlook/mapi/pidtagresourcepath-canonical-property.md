---
title: Propriedade canônica PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330167"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="5d109-103">Propriedade canônica PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="5d109-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="5d109-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d109-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d109-105">Contém um caminho para o servidor do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5d109-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d109-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5d109-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d109-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="5d109-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="5d109-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5d109-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d109-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="5d109-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="5d109-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5d109-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d109-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5d109-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5d109-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5d109-112">Area:</span></span>  <br/> |<span data-ttu-id="5d109-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="5d109-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d109-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d109-114">Remarks</span></span>

<span data-ttu-id="5d109-115">O caminho contido nessas propriedades representa o caminho sugerido onde o usuário pode encontrar recursos.</span><span class="sxs-lookup"><span data-stu-id="5d109-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="5d109-116">A definição dessas propriedades é específica do provedor.</span><span class="sxs-lookup"><span data-stu-id="5d109-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="5d109-117">Por exemplo, um aplicativo de agendamento usa essas propriedades para especificar o local sugerido para seus arquivos de aplicativo de agendamento.</span><span class="sxs-lookup"><span data-stu-id="5d109-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="5d109-118">O perfil de usuário de mensagens fornece essas propriedades como conveniência para que um aplicativo cliente não precise solicitar ao usuário de mensagens um caminho de rede ou uma letra de unidade de rede.</span><span class="sxs-lookup"><span data-stu-id="5d109-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="5d109-119">O MAPI funciona somente com nomes de fileno conjunto de caracteres ANSI (American National Standards Institute).</span><span class="sxs-lookup"><span data-stu-id="5d109-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="5d109-120">Os aplicativos que usam nomes de FileNames em um conjunto de caracteres OEM (fabricante original do equipamento) devem convertê-los para ANSI antes de chamar MAPI.</span><span class="sxs-lookup"><span data-stu-id="5d109-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d109-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d109-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5d109-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d109-122">Header files</span></span>

<span data-ttu-id="5d109-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5d109-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d109-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5d109-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d109-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5d109-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5d109-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5d109-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d109-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d109-127">See also</span></span>



[<span data-ttu-id="5d109-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5d109-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d109-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5d109-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d109-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5d109-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d109-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5d109-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

