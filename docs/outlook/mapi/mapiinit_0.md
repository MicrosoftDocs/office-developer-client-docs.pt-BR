---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 31b2353b76bbac5cd58cd791f4a289c7dbabdb78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767978"
---
# <a name="mapiinit0"></a><span data-ttu-id="6cfd3-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="6cfd3-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="6cfd3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6cfd3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6cfd3-105">Transmite opções para a função [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="6cfd3-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cfd3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6cfd3-106">Header file:</span></span>  <br/> |<span data-ttu-id="6cfd3-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="6cfd3-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="6cfd3-108">Members</span><span class="sxs-lookup"><span data-stu-id="6cfd3-108">Members</span></span>

 <span data-ttu-id="6cfd3-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="6cfd3-109">**ulVersion**</span></span>
  
> <span data-ttu-id="6cfd3-110">Um valor inteiro que representa o número de versão da estrutura **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="6cfd3-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="6cfd3-111">O membro **ulVersion** é para expansão futura e não representam a versão da interface do MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="6cfd3-112">Atualmente, **ulVersion** deve ser definida como MAPI_INIT_VERSION.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="6cfd3-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6cfd3-113">**ulFlags**</span></span>
  
> <span data-ttu-id="6cfd3-114">A bitmask dos sinalizadores usados para controlar a inicialização da sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="6cfd3-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="6cfd3-115">The following flags can be set:</span></span>
    
<span data-ttu-id="6cfd3-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="6cfd3-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="6cfd3-117">MAPI deve gerar notificações usando um thread dedicado a notificação manipulação em vez do primeiro segmento usado para chamar **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="6cfd3-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="6cfd3-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="6cfd3-119">O chamador está sendo executado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="6cfd3-120">Chamadores que não estejam executando um serviço do Windows não deve definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="6cfd3-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="6cfd3-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="6cfd3-122">Defina o sinalizador MAPI_NO_COINT para que **MAPIInitialize** não tenta inicializar COM uma chamada a [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6cfd3-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="6cfd3-123">Se uma estrutura **MAPIINIT_0** é passada para **MAPIInitialize** com _ulFlags_ definido como MAPI_NO_COINIT, MAPI partirá do pressuposto de que COM já foi inicializado e ignora a chamada para **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6cfd3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cfd3-124">Remarks</span></span>

<span data-ttu-id="6cfd3-125">Clientes multithreaded devem definir o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="6cfd3-126">Se o sinalizador não estiver definido, as notificações são geradas no thread usado para tornar a primeira chamada para **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="6cfd3-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="6cfd3-127">Para obter mais informações sobre quando definir esse sinalizador e como implementar a segurança do thread em um cliente, consulte [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="6cfd3-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6cfd3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cfd3-128">See also</span></span>



[<span data-ttu-id="6cfd3-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="6cfd3-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="6cfd3-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="6cfd3-130">MAPI Structures</span></span>](mapi-structures.md)
