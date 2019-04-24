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
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348696"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="6c54c-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="6c54c-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="6c54c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c54c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c54c-105">Abre um objeto status.</span><span class="sxs-lookup"><span data-stu-id="6c54c-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="6c54c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c54c-106">Parameters</span></span>

 <span data-ttu-id="6c54c-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6c54c-107">_lpInterface_</span></span>
  
> <span data-ttu-id="6c54c-108">no Um ponteiro para o identificador de interface (IID) do objeto status a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="6c54c-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="6c54c-109">Passar NULL indica que a interface padrão para o objeto é retornada (neste caso, a interface [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="6c54c-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="6c54c-110">O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto.</span><span class="sxs-lookup"><span data-stu-id="6c54c-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="6c54c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c54c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="6c54c-112">no Uma bitmask de sinalizadores que controla como o objeto status é aberto.</span><span class="sxs-lookup"><span data-stu-id="6c54c-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="6c54c-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6c54c-113">The following flag can be set:</span></span>
    
<span data-ttu-id="6c54c-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6c54c-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6c54c-115">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6c54c-115">Requests read/write permission.</span></span> <span data-ttu-id="6c54c-116">Por padrão, os objetos são criados com permissão somente leitura, e os aplicativos cliente não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="6c54c-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="6c54c-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6c54c-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="6c54c-118">bota Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="6c54c-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="6c54c-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="6c54c-119">_lppEntry_</span></span>
  
> <span data-ttu-id="6c54c-120">bota Um ponteiro para o ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="6c54c-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c54c-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6c54c-121">Return value</span></span>

<span data-ttu-id="6c54c-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c54c-122">S_OK</span></span> 
  
> <span data-ttu-id="6c54c-123">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="6c54c-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c54c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c54c-124">Remarks</span></span>

<span data-ttu-id="6c54c-125">Os provedores de repositórios de mensagens implementam o método **IMSLogon:: OpenStatusEntry** para abrir um objeto status.</span><span class="sxs-lookup"><span data-stu-id="6c54c-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="6c54c-126">Esse objeto status é usado para permitir que os clientes chamem métodos [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="6c54c-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="6c54c-127">Por exemplo, os clientes podem usar o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para reconfigurar a sessão de logon do repositório de mensagens ou o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) para validar o estado da sessão de logon do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6c54c-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c54c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c54c-128">See also</span></span>



[<span data-ttu-id="6c54c-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6c54c-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="6c54c-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="6c54c-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="6c54c-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="6c54c-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="6c54c-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c54c-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

