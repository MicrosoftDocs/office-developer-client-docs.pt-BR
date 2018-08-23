---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6b07d794a8f54477c6706cb70af60f7f7ef57d49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595339"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="c3b35-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="c3b35-103">MAPICrashRecovery</span></span>

<span data-ttu-id="c3b35-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3b35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3b35-105">A função de **MAPICrashRecovery** verifica que o estado do arquivo de pastas particulares (. PST) ou o arquivo de pastas Offline (OST) a memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="c3b35-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="c3b35-106">Se a memória estiver em um estado consistente, a função **MAPICrashRecovery** move os dados em disco e impede que o maior acesso de leitura ou gravação até que o processo é encerrado.</span><span class="sxs-lookup"><span data-stu-id="c3b35-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c3b35-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c3b35-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3b35-108">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="c3b35-108">Exported by:</span></span>  <br/> |<span data-ttu-id="c3b35-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c3b35-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c3b35-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="c3b35-110">Called by:</span></span>  <br/> |<span data-ttu-id="c3b35-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="c3b35-111">Client</span></span>  <br/> |
|<span data-ttu-id="c3b35-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="c3b35-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c3b35-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="c3b35-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="c3b35-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3b35-114">Parameters</span></span>

<span data-ttu-id="c3b35-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3b35-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c3b35-116">[in] Sinalizadores usados para controlar como a recuperação de travamento MAPI é executada.</span><span class="sxs-lookup"><span data-stu-id="c3b35-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="c3b35-117">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c3b35-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="c3b35-118">**MAPICRASH\_recuperar**: se o PSTs ou OSTs estiverem em um estado consistente, mover os dados em disco e bloquear o PSTs ou OSTs para impedir o acesso de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="c3b35-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="c3b35-119">**MAPICRASH\_continuar**: desbloquear o PSTs ou OSTs para depuração.</span><span class="sxs-lookup"><span data-stu-id="c3b35-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="c3b35-120">Após uma chamada bem sucedida para **MAPICrashRecovery** com o sinalizador **MAPICRASH_RECOVER** , chamar **MAPICrashRecovery** com o **MAPICRASH\_continuar** sinalizador para permitir depuração continuar.</span><span class="sxs-lookup"><span data-stu-id="c3b35-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="c3b35-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: se o PSTs ou OSTs estiverem em um estado consistente, mover os dados em disco e bloquear o PSTs ou OSTs para impedir o acesso de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="c3b35-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="c3b35-122">O PSTs ou OSTs não podem ser desbloqueados usando **MAPICRASH\_continuar**.</span><span class="sxs-lookup"><span data-stu-id="c3b35-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="c3b35-123">Deve ser usado em combinação com **MAPICRASH\_recuperar**.</span><span class="sxs-lookup"><span data-stu-id="c3b35-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c3b35-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3b35-124">Remarks</span></span>

<span data-ttu-id="c3b35-125">O byte superior (0xFF000000) é reservado para sinalizadores de recuperação de travamento específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="c3b35-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="c3b35-126">Chamar **MAPICrashRecovery** com o **MAPICRASH\_recuperar** e os sinalizadores **MAPICRASH_SYSTEM_SHUTDOWN** em resposta à mensagem **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="c3b35-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3b35-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3b35-127">See also</span></span>

- [<span data-ttu-id="c3b35-128">Sobre a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="c3b35-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="c3b35-129">Usar a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="c3b35-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

