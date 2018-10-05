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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389103"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="e3f9a-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3f9a-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="e3f9a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3f9a-105">Provedor de armazenamento de recursos de acessos de um arquivo de pastas particulares (. PST).</span><span class="sxs-lookup"><span data-stu-id="e3f9a-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3f9a-106">Herda de:</span><span class="sxs-lookup"><span data-stu-id="e3f9a-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="e3f9a-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3f9a-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="e3f9a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e3f9a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3f9a-109">Provedor de repositórios de PST</span><span class="sxs-lookup"><span data-stu-id="e3f9a-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="e3f9a-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e3f9a-110">Called by:</span></span>  <br/> |<span data-ttu-id="e3f9a-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="e3f9a-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="e3f9a-112">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="e3f9a-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e3f9a-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="e3f9a-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e3f9a-114">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="e3f9a-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e3f9a-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="e3f9a-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="e3f9a-116">Inicia o procedimento desbloqueando um arquivo de pastas particulares (. pst).</span><span class="sxs-lookup"><span data-stu-id="e3f9a-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3f9a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3f9a-117">Remarks</span></span>

<span data-ttu-id="e3f9a-118">Os identificadores de Interface de manipulador substituir PST não poderão ser definidos no arquivo de cabeçalho para download que você possui atualmente, caso em que você irá encontrá-las no tópico [Constantes MAPI](mapi-constants.md) e pode copiar e adicioná-los ao seu código.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="e3f9a-119">Use a macro DEFINE_GUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar nomes simbólicos de identificador globalmente exclusivo (GUID) com seus valores.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="e3f9a-120">Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="e3f9a-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3f9a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3f9a-121">See also</span></span>



[<span data-ttu-id="e3f9a-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3f9a-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

