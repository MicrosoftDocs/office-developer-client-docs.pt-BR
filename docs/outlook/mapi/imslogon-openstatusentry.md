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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 55cf41d251db4c84dad9f12d8f83d0b0dda63ff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767535"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="0e8e7-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="0e8e7-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="0e8e7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e8e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e8e7-105">Abre um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="0e8e7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0e8e7-106">Parameters</span></span>

 <span data-ttu-id="0e8e7-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0e8e7-107">_lpInterface_</span></span>
  
> <span data-ttu-id="0e8e7-108">[in] Um ponteiro para o identificador de interface (IID) para o objeto de status abrir.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="0e8e7-109">Passar NULL indica que a interface padrão para o objeto é retornada (no caso, a interface [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="0e8e7-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="0e8e7-110">O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="0e8e7-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e8e7-111">_ulFlags_</span></span>
  
> <span data-ttu-id="0e8e7-112">[in] Uma bitmask dos sinalizadores que controla como o objeto de status é aberto.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="0e8e7-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="0e8e7-113">The following flag can be set:</span></span>
    
<span data-ttu-id="0e8e7-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0e8e7-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0e8e7-115">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-115">Requests read/write permission.</span></span> <span data-ttu-id="0e8e7-116">Por padrão, são criados objetos com permissão somente leitura e aplicativos cliente não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="0e8e7-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0e8e7-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="0e8e7-118">[out] Um ponteiro para o tipo de objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="0e8e7-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="0e8e7-119">_lppEntry_</span></span>
  
> <span data-ttu-id="0e8e7-120">[out] Um ponteiro para o ponteiro para o objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e8e7-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0e8e7-121">Return value</span></span>

<span data-ttu-id="0e8e7-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e8e7-122">S_OK</span></span> 
  
> <span data-ttu-id="0e8e7-123">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e8e7-124">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0e8e7-124">Remarks</span></span>

<span data-ttu-id="0e8e7-125">Provedores de armazenamento de mensagem implementam o método **IMSLogon::OpenStatusEntry** para abrir um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="0e8e7-126">Este objeto de status é usado para permitir que os clientes chamar métodos [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8e7-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="0e8e7-127">Por exemplo, os clientes podem usar o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para reconfigurar a sessão de logon do repositório de mensagem ou o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para validar o estado da sessão de logon do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0e8e7-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e8e7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e8e7-128">See also</span></span>



[<span data-ttu-id="0e8e7-129">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0e8e7-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="0e8e7-130">IMAPIStatus:: SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="0e8e7-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="0e8e7-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="0e8e7-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="0e8e7-132">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e8e7-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

