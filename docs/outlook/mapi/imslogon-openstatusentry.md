---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571196"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="a5724-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a5724-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="a5724-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5724-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5724-105">Abre um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="a5724-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="a5724-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5724-106">Parameters</span></span>

 <span data-ttu-id="a5724-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a5724-107">_lpInterface_</span></span>
  
> <span data-ttu-id="a5724-108">[in] Um ponteiro para o identificador de interface (IID) para o objeto de status abrir.</span><span class="sxs-lookup"><span data-stu-id="a5724-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="a5724-109">Passar NULL indica que a interface padrão para o objeto é retornada (no caso, a interface [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="a5724-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="a5724-110">O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a5724-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="a5724-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5724-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a5724-112">[in] Uma bitmask dos sinalizadores que controla como o objeto de status é aberto.</span><span class="sxs-lookup"><span data-stu-id="a5724-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="a5724-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="a5724-113">The following flag can be set:</span></span>
    
<span data-ttu-id="a5724-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a5724-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a5724-115">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="a5724-115">Requests read/write permission.</span></span> <span data-ttu-id="a5724-116">Por padrão, são criados objetos com permissão somente leitura e aplicativos cliente não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a5724-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a5724-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="a5724-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="a5724-118">[out] Um ponteiro para o tipo de objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="a5724-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="a5724-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="a5724-119">_lppEntry_</span></span>
  
> <span data-ttu-id="a5724-120">[out] Um ponteiro para o ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="a5724-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5724-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a5724-121">Return value</span></span>

<span data-ttu-id="a5724-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5724-122">S_OK</span></span> 
  
> <span data-ttu-id="a5724-123">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="a5724-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5724-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5724-124">Remarks</span></span>

<span data-ttu-id="a5724-125">Provedores de armazenamento de mensagem implementam o método **IMSLogon::OpenStatusEntry** para abrir um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="a5724-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="a5724-126">Este objeto de status é usado para permitir que os clientes chamar métodos [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="a5724-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="a5724-127">Por exemplo, os clientes podem usar o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para reconfigurar a sessão de logon do repositório de mensagem ou o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para validar o estado da sessão de logon do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a5724-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5724-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5724-128">See also</span></span>



[<span data-ttu-id="a5724-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a5724-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="a5724-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="a5724-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="a5724-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="a5724-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="a5724-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5724-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

