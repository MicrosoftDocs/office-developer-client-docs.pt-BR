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
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357299"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="a22ba-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="a22ba-103">MAPICrashRecovery</span></span>

<span data-ttu-id="a22ba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a22ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a22ba-105">A função **MAPICrashRecovery** verifica o estado do arquivo de pastas particulares (PST) ou da memória compartilhada do arquivo de pastas offline (OST).</span><span class="sxs-lookup"><span data-stu-id="a22ba-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="a22ba-106">Se a memória estiver em um estado consistente, a função **MAPICrashRecovery** moverá os dados para o disco e impedirá o acesso de leitura ou gravação adicional até que o processo seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="a22ba-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a22ba-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a22ba-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a22ba-108">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="a22ba-108">Exported by:</span></span>  <br/> |<span data-ttu-id="a22ba-109">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="a22ba-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="a22ba-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a22ba-110">Called by:</span></span>  <br/> |<span data-ttu-id="a22ba-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="a22ba-111">Client</span></span>  <br/> |
|<span data-ttu-id="a22ba-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a22ba-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a22ba-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="a22ba-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="a22ba-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a22ba-114">Parameters</span></span>

<span data-ttu-id="a22ba-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a22ba-115">_ulFlags_</span></span>
  
> <span data-ttu-id="a22ba-116">no Sinalizadores usados para controlar como a recuperação de falha MAPI é executada.</span><span class="sxs-lookup"><span data-stu-id="a22ba-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="a22ba-117">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a22ba-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="a22ba-118">**Recuperação\_de MAPICRASH**: se o PSTs ou o OSTs estiverem em um estado consistente, mova os dados para o disco e bloqueie os PSTs ou OSTs para evitar acesso de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="a22ba-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="a22ba-119">**MAPICRASH\_continuar**: Desbloqueie os PSTs ou OSTs para depuração.</span><span class="sxs-lookup"><span data-stu-id="a22ba-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="a22ba-120">Após uma chamada bem-sucedida para **MAPICrashRecovery** com o sinalizador **MAPICRASH_RECOVER** , chame **MAPICrashRecovery** com o **sinalizador\_MAPICRASH continue** para permitir a depuração continuar.</span><span class="sxs-lookup"><span data-stu-id="a22ba-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="a22ba-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: se o PSTs ou o OSTs estiverem em um estado consistente, mova os dados para o disco e bloqueie o PSTs ou OSTs para impedir o acesso de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="a22ba-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="a22ba-122">PSTs ou OSTs não podem ser desbloqueados usando o **MAPICRASH\_continue**.</span><span class="sxs-lookup"><span data-stu-id="a22ba-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="a22ba-123">Deve ser usado em combinação com **a\_recuperação do MAPICRASH**.</span><span class="sxs-lookup"><span data-stu-id="a22ba-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a22ba-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a22ba-124">Remarks</span></span>

<span data-ttu-id="a22ba-125">O byte superior (0xFF000000) é reservado para sinalizadores de recuperação de pane específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="a22ba-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="a22ba-126">Chame **MAPICrashRecovery** com os **sinalizadores\_MAPICRASH Recover** e **MAPICRASH_SYSTEM_SHUTDOWN** em resposta à mensagem **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="a22ba-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a22ba-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a22ba-127">See also</span></span>

- [<span data-ttu-id="a22ba-128">Sobre a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="a22ba-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="a22ba-129">Usar a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="a22ba-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

