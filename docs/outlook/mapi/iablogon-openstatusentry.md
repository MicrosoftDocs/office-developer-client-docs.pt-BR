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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349018"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="c9ffa-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="c9ffa-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="c9ffa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9ffa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9ffa-105">Abre o objeto status do provedor.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="c9ffa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9ffa-106">Parameters</span></span>

 <span data-ttu-id="c9ffa-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c9ffa-107">_lpInterface_</span></span>
  
> <span data-ttu-id="c9ffa-108">no Um ponteiro para o identificador de interface (IID) que representa a interface que deve ser usada para acessar o objeto status.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="c9ffa-109">Passar NULL retorna a interface padrão do objeto, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="c9ffa-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="c9ffa-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9ffa-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c9ffa-111">no Uma bitmask de sinalizadores que controla como o objeto status é aberto.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="c9ffa-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="c9ffa-112">The following flag can be set:</span></span>
    
<span data-ttu-id="c9ffa-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c9ffa-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c9ffa-114">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-114">Requests read/write permission.</span></span> <span data-ttu-id="c9ffa-115">Por padrão, os objetos são abertos com acesso somente leitura, e os chamadores não devem supor que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="c9ffa-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="c9ffa-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="c9ffa-117">bota Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="c9ffa-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="c9ffa-118">_lppEntry_</span></span>
  
> <span data-ttu-id="c9ffa-119">bota Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9ffa-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c9ffa-120">Return value</span></span>

<span data-ttu-id="c9ffa-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9ffa-121">S_OK</span></span> 
  
> <span data-ttu-id="c9ffa-122">A chamada foi bem-sucedida e o objeto status foi aberto.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9ffa-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9ffa-123">Remarks</span></span>

<span data-ttu-id="c9ffa-124">Os provedores de catálogos de endereços implementam o método **OpenStatusEntry** para conceder acesso ao objeto status.</span><span class="sxs-lookup"><span data-stu-id="c9ffa-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="c9ffa-125">Todos os provedores de catálogo de endereços são necessários para implementar um objeto de status que suporte, no mínimo, o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="c9ffa-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="c9ffa-126">Para mais informações, consulte [implementação do objeto de status](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c9ffa-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9ffa-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9ffa-127">See also</span></span>



[<span data-ttu-id="c9ffa-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c9ffa-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="c9ffa-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="c9ffa-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="c9ffa-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="c9ffa-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="c9ffa-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9ffa-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

