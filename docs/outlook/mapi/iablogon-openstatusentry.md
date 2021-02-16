---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410781"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="6442e-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="6442e-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="6442e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6442e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6442e-105">Abre o objeto de status do provedor.</span><span class="sxs-lookup"><span data-stu-id="6442e-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="6442e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6442e-106">Parameters</span></span>

 <span data-ttu-id="6442e-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6442e-107">_lpInterface_</span></span>
  
> <span data-ttu-id="6442e-108">[in] Um ponteiro para o IID (identificador de interface) que representa a interface que deve ser usada para acessar o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="6442e-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="6442e-109">Passar NULL retorna a interface padrão do objeto, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6442e-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="6442e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6442e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6442e-111">[in] Uma máscara de bits de sinalizadores que controla como o objeto de status é aberto.</span><span class="sxs-lookup"><span data-stu-id="6442e-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="6442e-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6442e-112">The following flag can be set:</span></span>
    
<span data-ttu-id="6442e-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6442e-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6442e-114">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6442e-114">Requests read/write permission.</span></span> <span data-ttu-id="6442e-115">Por padrão, os objetos são abertos com acesso somente leitura e os chamadores não devem presumir que a permissão de leitura/gravação foi concedida.</span><span class="sxs-lookup"><span data-stu-id="6442e-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="6442e-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6442e-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="6442e-117">[out] Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="6442e-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="6442e-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="6442e-118">_lppEntry_</span></span>
  
> <span data-ttu-id="6442e-119">[out] Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="6442e-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6442e-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6442e-120">Return value</span></span>

<span data-ttu-id="6442e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6442e-121">S_OK</span></span> 
  
> <span data-ttu-id="6442e-122">A chamada foi bem-sucedida e o objeto de status foi aberto.</span><span class="sxs-lookup"><span data-stu-id="6442e-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6442e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6442e-123">Remarks</span></span>

<span data-ttu-id="6442e-124">Os provedores de agendas **implementam o método OpenStatusEntry** para conceder acesso ao seu objeto de status.</span><span class="sxs-lookup"><span data-stu-id="6442e-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="6442e-125">Todos os provedores de livro de endereços são necessários para implementar um objeto de status que oferece suporte, no mínimo, ao método [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="6442e-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="6442e-126">Para obter mais informações, consulte [Implementação de objeto de status.](status-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="6442e-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6442e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6442e-127">See also</span></span>



[<span data-ttu-id="6442e-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6442e-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="6442e-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="6442e-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="6442e-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="6442e-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="6442e-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6442e-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

