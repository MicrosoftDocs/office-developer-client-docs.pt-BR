---
title: Sobre a API de recuperação de falhas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576586"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="f8e5c-103">Sobre a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="f8e5c-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="f8e5c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8e5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8e5c-105">A API de recuperação MAPI travar verifica que o estado do arquivo de pastas particulares (. PST) ou o arquivo de pastas Offline (OST) compartilhado de memória para verificar se os dados estão em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="f8e5c-106">Se ele estiver em um estado consistente, a função [MAPICrashRecovery](mapicrashrecovery.md) move os dados do open PSTs ou OSTs em disco e bloqueia o PSTs ou OSTs e não permitir que qualquer acesso de leitura ou gravação aos dados.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="f8e5c-107">Isso garante que os dados permaneçam em um estado consistente, até que o processo é encerrado.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="f8e5c-108">Garantindo que o PSTs ou OSTs estão em um estado consistente antes do processo é encerrado, você pode impedir que o Microsoft Outlook 2013 e o Microsoft Outlook 2010 exiba a seguinte mensagem de erro e evitar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="f8e5c-109">**Um arquivo de dados não foi fechado corretamente a última vez que foi usada e está sendo verificada para problemas. Desempenho poderá ser afetado enquanto a seleção estiver em andamento.**</span><span class="sxs-lookup"><span data-stu-id="f8e5c-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="f8e5c-110">Essa API oferece os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="f8e5c-110">This API provides the following:</span></span>
  
<span data-ttu-id="f8e5c-111">Constantes:</span><span class="sxs-lookup"><span data-stu-id="f8e5c-111">Constants:</span></span>
  
- [<span data-ttu-id="f8e5c-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f8e5c-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="f8e5c-113">Funções:</span><span class="sxs-lookup"><span data-stu-id="f8e5c-113">Functions:</span></span>
  
- [<span data-ttu-id="f8e5c-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="f8e5c-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="f8e5c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8e5c-115">See also</span></span>



[<span data-ttu-id="f8e5c-116">Usar a API de recuperação de falhas MAPI</span><span class="sxs-lookup"><span data-stu-id="f8e5c-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

