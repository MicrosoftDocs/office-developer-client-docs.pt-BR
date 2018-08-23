---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7cb77308ebc7229adcab290fc8e1f9e11ce45065
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587016"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="d52ee-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="d52ee-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="d52ee-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d52ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d52ee-105">Abre o objeto de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="d52ee-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="d52ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d52ee-106">Parameters</span></span>

 <span data-ttu-id="d52ee-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d52ee-107">_lpInterface_</span></span>
  
> <span data-ttu-id="d52ee-108">[in] Um ponteiro para um identificador de interface (IID) para o objeto de logon de transporte.</span><span class="sxs-lookup"><span data-stu-id="d52ee-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="d52ee-109">Passar NULL retorna a interface de [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="d52ee-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="d52ee-110">O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d52ee-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="d52ee-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d52ee-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d52ee-112">[in] Uma bitmask dos sinalizadores que controla como o objeto de status é aberto.</span><span class="sxs-lookup"><span data-stu-id="d52ee-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="d52ee-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="d52ee-113">The following flag can be set:</span></span>
    
<span data-ttu-id="d52ee-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d52ee-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d52ee-115">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="d52ee-115">Requests read/write permission.</span></span> <span data-ttu-id="d52ee-116">A interface padrão é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d52ee-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="d52ee-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="d52ee-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="d52ee-118">[out] Um ponteiro para o tipo de objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="d52ee-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="d52ee-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="d52ee-119">_lppEntry_</span></span>
  
> <span data-ttu-id="d52ee-120">[out] Um ponteiro para o ponteiro para o objeto de status aberto.</span><span class="sxs-lookup"><span data-stu-id="d52ee-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d52ee-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d52ee-121">Return value</span></span>

<span data-ttu-id="d52ee-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d52ee-122">S_OK</span></span> 
  
> <span data-ttu-id="d52ee-123">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="d52ee-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d52ee-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d52ee-124">Remarks</span></span>

<span data-ttu-id="d52ee-125">O MAPI spooler chama o método de **IXPLogon::OpenStatusEntry** quando um aplicativo cliente chama um método **OpenEntry** para o identificador de entrada na linha de tabela de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="d52ee-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="d52ee-126">**OpenStatusEntry** abre um objeto com a interface de **IMAPIStatus** associada a esse logon do provedor de transporte específica.</span><span class="sxs-lookup"><span data-stu-id="d52ee-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="d52ee-127">Este objeto é usado para permitir que os aplicativos de cliente chamar métodos **IMAPIStatus** (por exemplo, para reconfigurar a sessão de logon usando o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) ou para validar o estado de sessão usando o [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) método).</span><span class="sxs-lookup"><span data-stu-id="d52ee-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d52ee-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d52ee-128">See also</span></span>



[<span data-ttu-id="d52ee-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d52ee-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="d52ee-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d52ee-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

