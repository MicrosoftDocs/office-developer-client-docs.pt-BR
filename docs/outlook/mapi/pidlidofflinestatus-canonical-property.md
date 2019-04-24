---
title: Propriedade canônica PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326296"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="97efc-103">Propriedade canônica PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="97efc-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="97efc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97efc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97efc-105">Determina o estado de um arquivo de documento em um servidor que implementa [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="97efc-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97efc-106">Propriedades associadas</span><span class="sxs-lookup"><span data-stu-id="97efc-106">Associated properties</span></span>  <br/> |<span data-ttu-id="97efc-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="97efc-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="97efc-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="97efc-108">Property set:</span></span>  <br/> |<span data-ttu-id="97efc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="97efc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="97efc-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="97efc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="97efc-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="97efc-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="97efc-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="97efc-112">Data type:</span></span>  <br/> |<span data-ttu-id="97efc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="97efc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="97efc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="97efc-114">Area:</span></span>  <br/> |<span data-ttu-id="97efc-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="97efc-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97efc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="97efc-116">Remarks</span></span>

<span data-ttu-id="97efc-117">A tabela a seguir mostra os valores possíveis dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="97efc-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="97efc-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="97efc-118">**Value**</span></span>|<span data-ttu-id="97efc-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="97efc-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97efc-120">,0</span><span class="sxs-lookup"><span data-stu-id="97efc-120">0</span></span>  <br/> |<span data-ttu-id="97efc-121">Não foi feito o check-out do documento.</span><span class="sxs-lookup"><span data-stu-id="97efc-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="97efc-122">1</span><span class="sxs-lookup"><span data-stu-id="97efc-122">1</span></span>  <br/> |<span data-ttu-id="97efc-123">O documento está com check-out para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="97efc-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="97efc-124">duas</span><span class="sxs-lookup"><span data-stu-id="97efc-124">2</span></span>  <br/> |<span data-ttu-id="97efc-125">Não foi feito o check-out do documento, mas o usuário atual tem uma cópia do arquivo salvo para edição no computador atual.</span><span class="sxs-lookup"><span data-stu-id="97efc-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="97efc-126">Essa propriedade é calculada localmente e não é enviada a um servidor a qualquer momento, a menos que um usuário arraste o item para outra conta.</span><span class="sxs-lookup"><span data-stu-id="97efc-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="97efc-127">Nesse caso, ele é tratado como uma propriedade personalizada definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="97efc-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97efc-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="97efc-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97efc-129">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="97efc-129">Protocol specifications</span></span>

<span data-ttu-id="97efc-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="97efc-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="97efc-131">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="97efc-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97efc-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="97efc-132">Header files</span></span>

<span data-ttu-id="97efc-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="97efc-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="97efc-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="97efc-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97efc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="97efc-135">See also</span></span>



[<span data-ttu-id="97efc-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="97efc-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97efc-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="97efc-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97efc-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="97efc-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97efc-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="97efc-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

