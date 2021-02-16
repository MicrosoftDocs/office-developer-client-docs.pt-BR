---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315495"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="f6238-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6238-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="f6238-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6238-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6238-105">Permite que um provedor de armazenamento de pastas particulares (PST) substitua a política PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="f6238-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6238-106">Herda de:</span><span class="sxs-lookup"><span data-stu-id="f6238-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="f6238-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6238-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="f6238-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f6238-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f6238-109">Provedor de armazenamento PST</span><span class="sxs-lookup"><span data-stu-id="f6238-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="f6238-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f6238-110">Called by:</span></span>  <br/> |<span data-ttu-id="f6238-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="f6238-111">Client</span></span>  <br/> |
|<span data-ttu-id="f6238-112">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="f6238-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f6238-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="f6238-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f6238-114">Vtable order</span><span class="sxs-lookup"><span data-stu-id="f6238-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f6238-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="f6238-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="f6238-116">Recupera a lista de registros do arquivo de Pastas Particulares (.pst).</span><span class="sxs-lookup"><span data-stu-id="f6238-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="f6238-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="f6238-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="f6238-118">Registra arquivos de Pastas Particulares para desbloqueio automático, evitando chamadas para HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="f6238-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="f6238-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="f6238-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="f6238-120">Desbloqueia um arquivo de Pastas Particulares para crescimento.</span><span class="sxs-lookup"><span data-stu-id="f6238-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6238-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6238-121">Remarks</span></span>

<span data-ttu-id="f6238-122">Os Identificadores da Interface do Manipulador de Substituição de PST podem não estar definidos no arquivo de header baixável que você tem atualmente, nesse caso, você os encontrará no tópico Constantes de [MAPI](mapi-constants.md) e poderá copiá-los e adicioná-los ao seu código.</span><span class="sxs-lookup"><span data-stu-id="f6238-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="f6238-123">Use a DEFINE_GUID macro definida no arquivo de título guiddef.h do Microsoft Software Development Kit do Windows (SDK) para associar nomes simbólicos de identificador global exclusivo (GUID) a seus valores.</span><span class="sxs-lookup"><span data-stu-id="f6238-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="f6238-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="f6238-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6238-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6238-125">See also</span></span>



[<span data-ttu-id="f6238-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6238-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

