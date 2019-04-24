---
title: Excluir um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316825"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="6101e-103">Excluir um perfil</span><span class="sxs-lookup"><span data-stu-id="6101e-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="6101e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6101e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6101e-105">**Para excluir um perfil**</span><span class="sxs-lookup"><span data-stu-id="6101e-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="6101e-106">Chamar [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="6101e-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="6101e-107">**DeleteProfile** marca o perfil para exclusão, se estiver sendo usado no momento, aguardando até que não esteja mais ativo para removê-lo.</span><span class="sxs-lookup"><span data-stu-id="6101e-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="6101e-108">O perfil não desaparece, de fato, até que todos os clientes com uma sessão ativa tenham sido desconectados.</span><span class="sxs-lookup"><span data-stu-id="6101e-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="6101e-109">**DeleteProfile** chama a função de ponto de entrada de cada serviço de mensagens no perfil com o parâmetro _ULCONTEXT_ definido como MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="6101e-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="6101e-110">As chamadas para as funções de ponto de entrada ocorrem antes de os serviços serem removidos fisicamente do perfil.</span><span class="sxs-lookup"><span data-stu-id="6101e-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

