---
title: Exclusão de um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766384"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="d9f43-103">Exclusão de um perfil</span><span class="sxs-lookup"><span data-stu-id="d9f43-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="d9f43-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9f43-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d9f43-105">**Para excluir um perfil**</span><span class="sxs-lookup"><span data-stu-id="d9f43-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="d9f43-106">Chame [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="d9f43-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="d9f43-107">**DeleteProfile** marca o perfil para exclusão, se ele está sendo usado atualmente, aguardar até que ele não está mais ativo para removê-lo.</span><span class="sxs-lookup"><span data-stu-id="d9f43-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="d9f43-108">O perfil não desapareça realmente até que cada cliente com uma sessão ativa desconectado.</span><span class="sxs-lookup"><span data-stu-id="d9f43-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="d9f43-109">**DeleteProfile** chama a função do ponto de entrada de cada serviço de mensagem no perfil com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="d9f43-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="d9f43-110">As chamadas para as funções de ponto de entrada ocorrerem antes que os serviços são removidos fisicamente do perfil.</span><span class="sxs-lookup"><span data-stu-id="d9f43-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

