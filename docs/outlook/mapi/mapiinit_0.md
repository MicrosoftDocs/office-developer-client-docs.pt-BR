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
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357292"
---
# <a name="mapiinit_0"></a><span data-ttu-id="531fe-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="531fe-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="531fe-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="531fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="531fe-105">Transmite opções para a [função MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="531fe-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="531fe-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="531fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="531fe-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="531fe-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="531fe-108">Members</span><span class="sxs-lookup"><span data-stu-id="531fe-108">Members</span></span>

 <span data-ttu-id="531fe-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="531fe-109">**ulVersion**</span></span>
  
> <span data-ttu-id="531fe-110">Um valor inteiro que representa o número de versão do **MAPIINIT_0** estrutura.</span><span class="sxs-lookup"><span data-stu-id="531fe-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="531fe-111">O **membro ulVersion** é para expansão futura e não representa a versão da interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="531fe-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="531fe-112">Atualmente, **ulVersion** deve ser definido como MAPI_INIT_VERSION.</span><span class="sxs-lookup"><span data-stu-id="531fe-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="531fe-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="531fe-113">**ulFlags**</span></span>
  
> <span data-ttu-id="531fe-114">A máscara de bits de sinalizadores usada para controlar a inicialização da sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="531fe-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="531fe-115">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="531fe-115">The following flags can be set:</span></span>
    
<span data-ttu-id="531fe-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="531fe-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="531fe-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="531fe-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="531fe-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="531fe-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="531fe-119">O chamador está sendo executado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="531fe-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="531fe-120">Os chamadores que não estão sendo executados como um serviço do Windows não devem definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="531fe-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="531fe-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="531fe-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="531fe-122">De definida MAPI_NO_COINT sinalizador para que **MAPIInitialize** não tente inicializar COM com uma chamada para [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="531fe-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="531fe-123">Se uma estrutura **MAPIINIT_0** for passada para **MAPIInitialize** com  _ulFlags_ definido como MAPI_NO_COINIT, o MAPI assumirá que COM já foi inicializado e ignorará a chamada para **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="531fe-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="531fe-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="531fe-124">Remarks</span></span>

<span data-ttu-id="531fe-125">Clientes multithreaded devem definir o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS leitura.</span><span class="sxs-lookup"><span data-stu-id="531fe-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="531fe-126">Se o sinalizador não estiver definido, as notificações serão geradas no thread usado para fazer a primeira chamada para **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="531fe-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="531fe-127">Para obter mais informações sobre quando definir esse sinalizador e como implementar a segurança de thread em um cliente, consulte [Threading em MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="531fe-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="531fe-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="531fe-128">See also</span></span>



[<span data-ttu-id="531fe-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="531fe-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="531fe-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="531fe-130">MAPI Structures</span></span>](mapi-structures.md)

