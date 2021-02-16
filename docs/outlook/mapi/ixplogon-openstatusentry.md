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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435898"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="4b831-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="4b831-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="4b831-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b831-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b831-105">Abre o objeto de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4b831-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="4b831-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b831-106">Parameters</span></span>

 <span data-ttu-id="4b831-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4b831-107">_lpInterface_</span></span>
  
> <span data-ttu-id="4b831-108">[in] Um ponteiro para um IID (identificador de interface) para o objeto de logon de transporte.</span><span class="sxs-lookup"><span data-stu-id="4b831-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="4b831-109">Passar NULL retorna a interface [IMAPIStatus.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="4b831-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="4b831-110">O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4b831-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="4b831-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b831-111">_ulFlags_</span></span>
  
> <span data-ttu-id="4b831-112">[in] Uma máscara de bits de sinalizadores que controla como o objeto de status é aberto.</span><span class="sxs-lookup"><span data-stu-id="4b831-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="4b831-113">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="4b831-113">The following flag can be set:</span></span>
    
<span data-ttu-id="4b831-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4b831-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4b831-115">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4b831-115">Requests read/write permission.</span></span> <span data-ttu-id="4b831-116">A interface padrão é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4b831-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="4b831-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="4b831-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="4b831-118">[out] Um ponteiro para o tipo do objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="4b831-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="4b831-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="4b831-119">_lppEntry_</span></span>
  
> <span data-ttu-id="4b831-120">[out] Um ponteiro para o ponteiro para o objeto de status aberto.</span><span class="sxs-lookup"><span data-stu-id="4b831-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b831-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4b831-121">Return value</span></span>

<span data-ttu-id="4b831-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b831-122">S_OK</span></span> 
  
> <span data-ttu-id="4b831-123">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="4b831-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b831-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b831-124">Remarks</span></span>

<span data-ttu-id="4b831-125">O spooler MAPI chama o método **IXPLogon::OpenStatusEntry** quando um aplicativo cliente chama um método **OpenEntry** para o identificador de entrada na linha da tabela de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4b831-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="4b831-126">**OpenStatusEntry** abre um objeto com a interface **IMAPIStatus** associada a esse logon específico do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4b831-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="4b831-127">Esse objeto é usado para permitir que aplicativos cliente chamem métodos **IMAPIStatus** (por exemplo, para reconfigurar a sessão de logon usando o método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou para validar o estado da sessão de logon usando o método [IMAPIStatus::ValidateState).](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="4b831-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b831-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b831-128">See also</span></span>



[<span data-ttu-id="4b831-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4b831-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="4b831-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b831-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

