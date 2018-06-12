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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766839"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="de637-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="de637-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="de637-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de637-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de637-105">Abre o objeto de status do provedor.</span><span class="sxs-lookup"><span data-stu-id="de637-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="de637-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="de637-106">Parameters</span></span>

 <span data-ttu-id="de637-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="de637-107">_lpInterface_</span></span>
  
> <span data-ttu-id="de637-108">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que deve ser usada para acessar o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="de637-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="de637-109">Passar NULL retorna a interface de padrão do objeto, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="de637-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="de637-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="de637-110">_ulFlags_</span></span>
  
> <span data-ttu-id="de637-111">[in] Uma bitmask dos sinalizadores que controla como o objeto de status é aberto.</span><span class="sxs-lookup"><span data-stu-id="de637-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="de637-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="de637-112">The following flag can be set:</span></span>
    
<span data-ttu-id="de637-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="de637-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="de637-114">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="de637-114">Requests read/write permission.</span></span> <span data-ttu-id="de637-115">Por padrão, os objetos são abertos com acesso somente leitura e os chamadores não devem presumir que foi concedida permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="de637-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="de637-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="de637-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="de637-117">[out] Um ponteiro para o tipo de objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="de637-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="de637-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="de637-118">_lppEntry_</span></span>
  
> <span data-ttu-id="de637-119">[out] Um ponteiro para um ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="de637-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de637-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="de637-120">Return value</span></span>

<span data-ttu-id="de637-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="de637-121">S_OK</span></span> 
  
> <span data-ttu-id="de637-122">A chamada foi bem-sucedida e o objeto de status tiver sido aberto.</span><span class="sxs-lookup"><span data-stu-id="de637-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de637-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="de637-123">Remarks</span></span>

<span data-ttu-id="de637-124">Provedores de catálogo de endereços implementam o método **OpenStatusEntry** para conceder acesso ao objeto seus status.</span><span class="sxs-lookup"><span data-stu-id="de637-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="de637-125">Todos os provedores de catálogo de endereços são necessários para implementar um objeto de status que suporta, no mínimo, o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="de637-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="de637-126">Para obter mais informações, consulte [Implementação do objeto de Status](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="de637-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de637-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="de637-127">See also</span></span>



[<span data-ttu-id="de637-128">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="de637-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="de637-129">IMAPIStatus:: SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="de637-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="de637-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="de637-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="de637-131">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="de637-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

