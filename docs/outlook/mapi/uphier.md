---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414918"
---
# <a name="uphier"></a><span data-ttu-id="345bd-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="345bd-103">UPHIER</span></span>
 
<span data-ttu-id="345bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="345bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="345bd-105">Informações para sincronizar uma hierarquia de pastas durante o estado [de hierarquia de carregamento.](upload-hierarchy-state.md)</span><span class="sxs-lookup"><span data-stu-id="345bd-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="345bd-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="345bd-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="345bd-107">Membros</span><span class="sxs-lookup"><span data-stu-id="345bd-107">Members</span></span>

<span data-ttu-id="345bd-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="345bd-108">_ulFlags_</span></span>
  
> <span data-ttu-id="345bd-109">[in] Sinalizadores para modificar o comportamento ao sincronizar a hierarquia de pastas.</span><span class="sxs-lookup"><span data-stu-id="345bd-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="345bd-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="345bd-110">UPH_OK</span></span>
    
    - <span data-ttu-id="345bd-111">[in] O carregamento foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="345bd-111">[in] Upload was successful.</span></span> <span data-ttu-id="345bd-112">O cliente define isso depois de carregar com êxito as informações para o servidor.</span><span class="sxs-lookup"><span data-stu-id="345bd-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="345bd-113">Ao ver esse sinalizador, o Outlook limpa todas as informações de manutenção contábil internas que indicavam que a hierarquia de pastas necessitava de atualização.</span><span class="sxs-lookup"><span data-stu-id="345bd-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="345bd-114">O cliente passa o HRESULT se o carregamento não foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="345bd-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="345bd-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="345bd-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="345bd-116">[out] Este membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="345bd-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="345bd-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="345bd-117">_iEnt_</span></span>
  
> <span data-ttu-id="345bd-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span><span class="sxs-lookup"><span data-stu-id="345bd-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="345bd-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="345bd-119">_cEnt_</span></span>
  
> <span data-ttu-id="345bd-120">[out] Número de pastas que estão fora de sincronia.</span><span class="sxs-lookup"><span data-stu-id="345bd-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="345bd-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="345bd-121">See also</span></span>

- [<span data-ttu-id="345bd-122">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="345bd-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="345bd-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="345bd-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="345bd-124">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="345bd-124">MAPI Constants</span></span>](mapi-constants.md)

