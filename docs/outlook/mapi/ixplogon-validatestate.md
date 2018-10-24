---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577482"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="1f3cf-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="1f3cf-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="1f3cf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f3cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f3cf-105">Verifica o status de externo do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1f3cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f3cf-106">Parameters</span></span>

 <span data-ttu-id="1f3cf-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1f3cf-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1f3cf-108">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="1f3cf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f3cf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1f3cf-110">[in] Uma bitmask dos sinalizadores que controla como a verificação de status é executada e os resultados da verificação de status.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="1f3cf-111">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="1f3cf-111">The following flags can be set:</span></span>
    
<span data-ttu-id="1f3cf-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="1f3cf-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="1f3cf-113">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="1f3cf-114">O provedor de transporte tem a opção para continuar trabalhando com a operação, ou pode anular a operação e retornar MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="1f3cf-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="1f3cf-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="1f3cf-116">Valida o estado dos provedores de transporte carregado no momento, fazendo com que o MAPI spooler ao chamar o método seus [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="1f3cf-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="1f3cf-117">Esse sinalizador também oferece o MAPI spooler uma oportunidade para corrigir falhas de provedor de transporte crítico sem forçar os aplicativos cliente de fazer logoff e logon novamente.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="1f3cf-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="1f3cf-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="1f3cf-119">O usuário selecionou uma operação de conexão.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-119">The user selected a connect operation.</span></span> <span data-ttu-id="1f3cf-120">Quando esse sinalizador é usado com o sinalizador REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, ocorre a ação de conectar sem cache.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="1f3cf-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="1f3cf-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="1f3cf-122">O usuário selecionou uma operação de desconexão.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="1f3cf-123">Quando esse sinalizador é usado com REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, ocorre a ação de desconexão sem cache.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="1f3cf-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="1f3cf-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="1f3cf-125">As entradas da tabela de cache de cabeçalho devem ser processadas, todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DOWNLOAD devem ser baixadas e todas as mensagens marcadas com o sinalizador MSGSTATUS_REMOTE_DELETE devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="1f3cf-126">Mensagens que tenham MSGSTATUS_REMOTE_DOWNLOAD e o MSGSTATUS_REMOTE_DELETE definido devem ser movidas.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="1f3cf-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="1f3cf-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="1f3cf-128">Uma nova lista de cabeçalhos de mensagem deve ser baixada e status de mensagem de todos os sinalizadores de marcação deve ser limpo.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="1f3cf-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="1f3cf-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="1f3cf-130">Impede que o provedor de transporte exiba uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1f3cf-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1f3cf-131">Return value</span></span>

<span data-ttu-id="1f3cf-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f3cf-132">S_OK</span></span> 
  
> <span data-ttu-id="1f3cf-133">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="1f3cf-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1f3cf-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1f3cf-135">Outra operação está em andamento. ele deve ter permissão para concluir ou deve ser interrompido antes que esta operação é tentada.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="1f3cf-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1f3cf-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1f3cf-137">O provedor de transporte remoto envolvido não dá suporte a uma interface do usuário e do próprio aplicativo cliente deve exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="1f3cf-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1f3cf-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1f3cf-139">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1f3cf-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f3cf-140">Remarks</span></span>

<span data-ttu-id="1f3cf-141">O MAPI spooler chama o método de **IXPLogon::ValidateState** para oferecer suporte a chamadas para o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="1f3cf-142">O provedor de transporte deve responder à chamada **IXPLogon::ValidateState** exatamente como se o MAPI spooler tinha aberto de um objeto de status para a sessão de logon atual e, em seguida, chamado **IMAPIStatus::ValidateState** nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="1f3cf-143">Para suportar sua implementação do **IMAPIStatus::ValidateState**, o MAPI spooler chama **IXPLogon::ValidateState** em todos os objetos de logon para todos os provedores de transporte ativo que estão executando em uma sessão de perfil.</span><span class="sxs-lookup"><span data-stu-id="1f3cf-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f3cf-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f3cf-144">See also</span></span>



[<span data-ttu-id="1f3cf-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="1f3cf-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="1f3cf-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="1f3cf-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="1f3cf-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f3cf-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

