---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419986"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="a5cc1-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="a5cc1-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="a5cc1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5cc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5cc1-105">Faz alterações em uma seção de perfil de armazenamento de mensagens permanente.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a5cc1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5cc1-106">Parameters</span></span>

 <span data-ttu-id="a5cc1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5cc1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a5cc1-108">[in] Uma máscara de bits de sinalizadores que indica o tipo de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="a5cc1-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="a5cc1-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a5cc1-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="a5cc1-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="a5cc1-111">O armazenamento de mensagens é temporário e não deve ser adicionado à tabela do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="a5cc1-112">Quando MDB_TEMPORARY é definido, **ModifyProfile** retorna S_OK imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a5cc1-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a5cc1-113">Return value</span></span>

<span data-ttu-id="a5cc1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5cc1-114">S_OK</span></span> 
  
> <span data-ttu-id="a5cc1-115">As alterações feitas na seção de perfil foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5cc1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5cc1-116">Remarks</span></span>

<span data-ttu-id="a5cc1-117">O **método IMAPISupport::ModifyProfile** é implementado para objetos de suporte do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="a5cc1-118">Os provedores de armazenamento de mensagens **chamam ModifyProfile** para solicitar que o MAPI modifique suas informações de perfil.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="a5cc1-119">**ModifyProfile adiciona** a seção de perfil associada ao provedor de chamada à lista de recursos instalados do provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="a5cc1-120">Isso faz com que o armazenamento de mensagens seja listado na tabela do armazenamento de mensagens, que está disponível para clientes por meio do método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) e ser aberto sem a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="a5cc1-121">Se o MDB_TEMPORARY de dados estiver definido, MAPI não faz nada e o método retorna imediatamente com S_OK.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5cc1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5cc1-122">See also</span></span>



[<span data-ttu-id="a5cc1-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="a5cc1-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="a5cc1-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5cc1-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

