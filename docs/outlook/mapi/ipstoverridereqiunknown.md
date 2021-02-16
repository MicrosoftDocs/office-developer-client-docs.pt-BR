---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356977"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="d185d-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d185d-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="d185d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d185d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d185d-105">Acessa recursos de um provedor de armazenamento de pastas particulares (PST).</span><span class="sxs-lookup"><span data-stu-id="d185d-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d185d-106">Herda de:</span><span class="sxs-lookup"><span data-stu-id="d185d-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="d185d-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d185d-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="d185d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d185d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d185d-109">Provedor de armazenamento PST</span><span class="sxs-lookup"><span data-stu-id="d185d-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="d185d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="d185d-110">Called by:</span></span>  <br/> |<span data-ttu-id="d185d-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="d185d-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="d185d-112">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="d185d-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d185d-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="d185d-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d185d-114">Vtable order</span><span class="sxs-lookup"><span data-stu-id="d185d-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d185d-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="d185d-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="d185d-116">Inicia o procedimento de desbloqueio para um arquivo de Pastas Particulares (.pst).</span><span class="sxs-lookup"><span data-stu-id="d185d-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d185d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d185d-117">Remarks</span></span>

<span data-ttu-id="d185d-118">Os Identificadores da Interface do Manipulador de Substituição de PST podem não estar definidos no arquivo de header baixável que você tem atualmente, nesse caso, você os encontrará no tópico Constantes de [MAPI](mapi-constants.md) e poderá copiá-los e adicioná-los ao seu código.</span><span class="sxs-lookup"><span data-stu-id="d185d-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="d185d-119">Use a DEFINE_GUID macro definida no arquivo de título guiddef.h do Microsoft Software Development Kit do Windows (SDK) para associar nomes simbólicos de identificador global exclusivo (GUID) a seus valores.</span><span class="sxs-lookup"><span data-stu-id="d185d-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="d185d-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="d185d-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d185d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d185d-121">See also</span></span>



[<span data-ttu-id="d185d-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d185d-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

