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
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="86ae8-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86ae8-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="86ae8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86ae8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86ae8-105">Acessa recursos de um provedor de repositório de arquivos de pastas particulares (PST).</span><span class="sxs-lookup"><span data-stu-id="86ae8-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86ae8-106">Herda de:</span><span class="sxs-lookup"><span data-stu-id="86ae8-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="86ae8-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="86ae8-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="86ae8-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="86ae8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="86ae8-109">Provedor de repositório PST</span><span class="sxs-lookup"><span data-stu-id="86ae8-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="86ae8-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="86ae8-110">Called by:</span></span>  <br/> |<span data-ttu-id="86ae8-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="86ae8-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="86ae8-112">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="86ae8-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="86ae8-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="86ae8-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="86ae8-114">Vtable order</span><span class="sxs-lookup"><span data-stu-id="86ae8-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="86ae8-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="86ae8-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="86ae8-116">Inicia o procedimento de desbloqueio para um arquivo de pastas particulares (. pst).</span><span class="sxs-lookup"><span data-stu-id="86ae8-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86ae8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="86ae8-117">Remarks</span></span>

<span data-ttu-id="86ae8-118">Os identificadores de interface do manipulador de substituição de PST podem não ser definidos no arquivo de cabeçalho que pode ser baixado e, nesse caso, você irá encontrá-los no tópico de [constantes de MAPI](mapi-constants.md) e pode copiá-los e adicioná-los ao seu código.</span><span class="sxs-lookup"><span data-stu-id="86ae8-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="86ae8-119">Use a macro DEFINE_GUID definida no arquivo de cabeçalho do Microsoft Windows Software Development Kit (SDK) guiddef. h para associar nomes simbólicos de identificador global exclusivo (GUID) a seus valores.</span><span class="sxs-lookup"><span data-stu-id="86ae8-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="86ae8-120">Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="86ae8-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86ae8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="86ae8-121">See also</span></span>



[<span data-ttu-id="86ae8-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86ae8-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

