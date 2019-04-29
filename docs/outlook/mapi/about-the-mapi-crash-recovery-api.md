---
title: Sobre a API de recuperação de falhas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420259"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="b51df-103">Sobre a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="b51df-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="b51df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b51df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b51df-105">A API de recuperação de falha MAPI verifica o estado do arquivo de pastas particulares (PST) ou da memória compartilhada do OST (arquivo de pastas offline) para verificar se os dados estão em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="b51df-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="b51df-106">Se estiver em um estado consistente, a função [MAPICrashRecovery](mapicrashrecovery.md) moverá os dados dos PSTs abertos ou OSTs para o disco e bloqueará os PSTs ou OSTs e não permitirá qualquer acesso de leitura ou gravação aos dados.</span><span class="sxs-lookup"><span data-stu-id="b51df-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="b51df-107">Isso garante que os dados permaneçam em um estado consistente até que o processo seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="b51df-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="b51df-108">Ao garantir que PSTs ou OSTs estejam em um estado consistente antes do término do processo, você pode impedir que o Microsoft Outlook 2013 e o Microsoft Outlook 2010 exibam a mensagem de erro a seguir e evitar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="b51df-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="b51df-109">**Um arquivo de dados não foi fechado corretamente na última vez em que foi usado e está sendo verificado em busca de problemas. O desempenho pode ser afetado enquanto o cheque estiver em andamento.**</span><span class="sxs-lookup"><span data-stu-id="b51df-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="b51df-110">Essa API fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b51df-110">This API provides the following:</span></span>
  
<span data-ttu-id="b51df-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="b51df-111">Constants:</span></span>
  
- [<span data-ttu-id="b51df-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b51df-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="b51df-113">Funções:</span><span class="sxs-lookup"><span data-stu-id="b51df-113">Functions:</span></span>
  
- [<span data-ttu-id="b51df-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="b51df-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="b51df-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b51df-115">See also</span></span>



[<span data-ttu-id="b51df-116">Usar a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="b51df-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

