---
title: Sobre o exemplo de suplemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a6bdf408-114a-2203-189f-101251a65a8c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf8e647af4aba53dfc24880e6ff491985b50a613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329775"
---
# <a name="about-the-sample-offline-state-add-in"></a><span data-ttu-id="5bfd9-103">Sobre o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="5bfd9-103">About the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="5bfd9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bfd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bfd9-105">A API de estado offline oferece suporte a retornos de chamada que indicam alterações no estado de conexão de um usuário no Outlook — por exemplo, de estar online no Outlook para offline.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-105">The Offline State API supports callbacks indicating changes in a user's connection state in Outlook—for example, from being online in Outlook to being offline.</span></span> <span data-ttu-id="5bfd9-106">O exemplo de suplemento offline State é um suplemento de COM escrito em C++ que demonstra como receber notificações de alterações de estado de conexão e como modificar o estado atual usando a API de estado offline.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-106">The Sample Offline State Add-in is a COM add-in written in C++ that demonstrates how to receive notifications of connection state changes and how to modify the current state using the Offline State API.</span></span> <span data-ttu-id="5bfd9-107">Confira mais informações sobre a API de Estado Offline em [Sobre a API de Estado Offline](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="5bfd9-107">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5bfd9-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5bfd9-108">In this section</span></span>

- [<span data-ttu-id="5bfd9-109">Instalar a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="5bfd9-109">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
    
- <span data-ttu-id="5bfd9-110">Explica como baixar e instalar o exemplo de suplemento de estado offline.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-110">Explains how to download and install the Sample Offline State Add-in.</span></span>
    
- [<span data-ttu-id="5bfd9-111">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="5bfd9-111">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
    
- <span data-ttu-id="5bfd9-112">Descreve como implementar funções de conexão, inicialização e configuração para usar um suplemento de estado offline.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-112">Describes how to implement connection, initialization, and setup functions in order to use an offline state add-in.</span></span>
    
- [<span data-ttu-id="5bfd9-113">Monitorar alterações de estado da conexão usando um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="5bfd9-113">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
    
- <span data-ttu-id="5bfd9-114">Descreve como usar a função **[HrOpenOfflineObj](hropenofflineobj.md)** para obter um objeto offline para monitorar e alterar o estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-114">Describes how to use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object to monitor and change the connection state.</span></span> 
    
- [<span data-ttu-id="5bfd9-115">Desconectar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="5bfd9-115">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)
    
- <span data-ttu-id="5bfd9-116">Descreve como encerrar e limpar corretamente um suplemento de estado offline quando o suplemento é desconectado.</span><span class="sxs-lookup"><span data-stu-id="5bfd9-116">Describes how to properly terminate and clean up an offline state add-in when the add-in is disconnected.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bfd9-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bfd9-117">See also</span></span>



[<span data-ttu-id="5bfd9-118">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="5bfd9-118">About the Offline State API</span></span>](about-the-offline-state-api.md)

