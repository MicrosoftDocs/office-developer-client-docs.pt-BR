---
title: Sobre o exemplo de suplemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a6bdf408-114a-2203-189f-101251a65a8c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dcb5d63e2f8b7b1371fbcf2d74f52c6bba84e6dc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569012"
---
# <a name="about-the-sample-offline-state-add-in"></a><span data-ttu-id="caa77-103">Sobre o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="caa77-103">About the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="caa77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caa77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caa77-105">A API de estado Offline oferece suporte a chamadas de retorno indicando alterações no estado de conexão de um usuário no Outlook — por exemplo, de sendo online no Outlook para sendo offline.</span><span class="sxs-lookup"><span data-stu-id="caa77-105">The Offline State API supports callbacks indicating changes in a user's connection state in Outlook—for example, from being online in Outlook to being offline.</span></span> <span data-ttu-id="caa77-106">O suplemento de amostra Offline estado é um suplemento de COM escritos em C++ que demonstra como receber notificações de alterações de estado de conexão e como modificar o estado atual usando o API de estado Offline.</span><span class="sxs-lookup"><span data-stu-id="caa77-106">The Sample Offline State Add-in is a COM add-in written in C++ that demonstrates how to receive notifications of connection state changes and how to modify the current state using the Offline State API.</span></span> <span data-ttu-id="caa77-107">Confira mais informações sobre a API de Estado Offline em [Sobre a API de Estado Offline](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="caa77-107">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="caa77-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="caa77-108">In this section</span></span>

- [<span data-ttu-id="caa77-109">Instalar a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="caa77-109">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
    
- <span data-ttu-id="caa77-110">Explica como baixar e instalar o suplemento de amostra Offline estado.</span><span class="sxs-lookup"><span data-stu-id="caa77-110">Explains how to download and install the Sample Offline State Add-in.</span></span>
    
- [<span data-ttu-id="caa77-111">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="caa77-111">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
    
- <span data-ttu-id="caa77-112">Descreve como implementar as funções de instalação, inicialização e conexão para usar um suplemento do estado offline.</span><span class="sxs-lookup"><span data-stu-id="caa77-112">Describes how to implement connection, initialization, and setup functions in order to use an offline state add-in.</span></span>
    
- [<span data-ttu-id="caa77-113">Monitorar alterações de estado da conexão usando um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="caa77-113">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
    
- <span data-ttu-id="caa77-114">Descreve como usar a função **[HrOpenOfflineObj](hropenofflineobj.md)** para obter um objeto offline para monitorar e alterar o estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="caa77-114">Describes how to use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object to monitor and change the connection state.</span></span> 
    
- [<span data-ttu-id="caa77-115">Desconectando um Offline suplemento State</span><span class="sxs-lookup"><span data-stu-id="caa77-115">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)
    
- <span data-ttu-id="caa77-116">Descreve como encerrar e limpar um suplemento do estado offline quando o suplemento é desconectado corretamente.</span><span class="sxs-lookup"><span data-stu-id="caa77-116">Describes how to properly terminate and clean up an offline state add-in when the add-in is disconnected.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="caa77-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="caa77-117">See also</span></span>



[<span data-ttu-id="caa77-118">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="caa77-118">About the Offline State API</span></span>](about-the-offline-state-api.md)

