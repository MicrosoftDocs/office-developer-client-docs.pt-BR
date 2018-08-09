---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 041ae867ff3a9cc9636ff1d93f9360576e455420
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770670"
---
# <a name="uphier"></a><span data-ttu-id="fe31a-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="fe31a-103">UPHIER</span></span>
 
<span data-ttu-id="fe31a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe31a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe31a-105">Informações para a sincronização de uma hierarquia de pastas durante o [carregamento do estado de hierarquia](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="fe31a-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fe31a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="fe31a-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="fe31a-107">Members</span><span class="sxs-lookup"><span data-stu-id="fe31a-107">Members</span></span>

<span data-ttu-id="fe31a-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fe31a-108">_ulFlags_</span></span>
  
> <span data-ttu-id="fe31a-109">[in] Sinalizadores para modificar o comportamento durante a sincronização de hierarquia de pastas.</span><span class="sxs-lookup"><span data-stu-id="fe31a-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="fe31a-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="fe31a-110">UPH_OK</span></span>
    
    - <span data-ttu-id="fe31a-111">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fe31a-111">[in] Upload was successful.</span></span> <span data-ttu-id="fe31a-112">O cliente define esta após carregar com êxito as informações para o servidor.</span><span class="sxs-lookup"><span data-stu-id="fe31a-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="fe31a-113">Após a vejam esse sinalizador, Outlook limpa qualquer informação de escrituração contábil interna que indicado que na hierarquia de pastas precisava ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="fe31a-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="fe31a-114">O cliente passa o HRESULT, se o carregamento não foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fe31a-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="fe31a-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="fe31a-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="fe31a-116">[out] Este membro é reservado para uso interno do Outlook e não é suportado.</span><span class="sxs-lookup"><span data-stu-id="fe31a-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="fe31a-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="fe31a-117">_iEnt_</span></span>
  
> <span data-ttu-id="fe31a-118">[out] Índice para controlar o número de pastas especificadas pela *cEnt* como sincronizar.</span><span class="sxs-lookup"><span data-stu-id="fe31a-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="fe31a-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="fe31a-119">_cEnt_</span></span>
  
> <span data-ttu-id="fe31a-120">[out] Número de pastas que estão fora de sincronia.</span><span class="sxs-lookup"><span data-stu-id="fe31a-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe31a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe31a-121">See also</span></span>

- [<span data-ttu-id="fe31a-122">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="fe31a-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="fe31a-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="fe31a-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="fe31a-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fe31a-124">MAPI Constants</span></span>](mapi-constants.md)

