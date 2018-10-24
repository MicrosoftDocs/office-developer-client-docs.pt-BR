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
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592091"
---
# <a name="uphier"></a><span data-ttu-id="d5689-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="d5689-103">UPHIER</span></span>
 
<span data-ttu-id="d5689-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5689-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5689-105">Informações para a sincronização de uma hierarquia de pastas durante o [carregamento do estado de hierarquia](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="d5689-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d5689-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d5689-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="d5689-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d5689-107">Members</span></span>

<span data-ttu-id="d5689-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5689-108">_ulFlags_</span></span>
  
> <span data-ttu-id="d5689-109">[in] Sinalizadores para modificar o comportamento durante a sincronização de hierarquia de pastas.</span><span class="sxs-lookup"><span data-stu-id="d5689-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="d5689-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="d5689-110">UPH_OK</span></span>
    
    - <span data-ttu-id="d5689-111">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d5689-111">[in] Upload was successful.</span></span> <span data-ttu-id="d5689-112">O cliente define esta após carregar com êxito as informações para o servidor.</span><span class="sxs-lookup"><span data-stu-id="d5689-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="d5689-113">Após a vejam esse sinalizador, Outlook limpa qualquer informação de escrituração contábil interna que indicado que na hierarquia de pastas precisava ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d5689-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="d5689-114">O cliente passa o HRESULT, se o carregamento não foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d5689-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="d5689-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="d5689-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="d5689-116">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="d5689-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="d5689-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="d5689-117">_iEnt_</span></span>
  
> <span data-ttu-id="d5689-118">[out] Índice para controlar o número de pastas especificadas pela *cEnt* como sincronizar.</span><span class="sxs-lookup"><span data-stu-id="d5689-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="d5689-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="d5689-119">_cEnt_</span></span>
  
> <span data-ttu-id="d5689-120">[out] Número de pastas que estão fora de sincronia.</span><span class="sxs-lookup"><span data-stu-id="d5689-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5689-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5689-121">See also</span></span>

- [<span data-ttu-id="d5689-122">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d5689-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d5689-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d5689-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d5689-124">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="d5689-124">MAPI Constants</span></span>](mapi-constants.md)

