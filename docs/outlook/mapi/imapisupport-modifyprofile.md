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
ms.openlocfilehash: b16730681b5414f28ae45be7195b4fa551bf0e82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591986"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="9d74d-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="9d74d-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="9d74d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d74d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d74d-105">Faz com que alterações a uma mensagem armazenar seção perfil permanente.</span><span class="sxs-lookup"><span data-stu-id="9d74d-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9d74d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d74d-106">Parameters</span></span>

 <span data-ttu-id="9d74d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d74d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9d74d-108">[in] Armazene em uma bitmask dos sinalizadores que indica o tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9d74d-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="9d74d-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9d74d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9d74d-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="9d74d-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="9d74d-111">O armazenamento de mensagens é temporário e não deve ser adicionado à tabela de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9d74d-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="9d74d-112">Quando MDB_TEMPORARY estiver definido, o **ModifyProfile** Retorna S_OK imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9d74d-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9d74d-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9d74d-113">Return value</span></span>

<span data-ttu-id="9d74d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d74d-114">S_OK</span></span> 
  
> <span data-ttu-id="9d74d-115">As alterações para a seção de perfil foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="9d74d-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d74d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d74d-116">Remarks</span></span>

<span data-ttu-id="9d74d-117">O método **IMAPISupport::ModifyProfile** é implementado para objetos de suporte do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9d74d-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9d74d-118">Mensagem de chamada de provedores de repositório **ModifyProfile** para solicitar o MAPI para modificar suas informações de perfil.</span><span class="sxs-lookup"><span data-stu-id="9d74d-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="9d74d-119">**ModifyProfile** adiciona a seção de perfil que está associada com o provedor de chamada à lista de recursos do provedor de repositório de mensagem instalado.</span><span class="sxs-lookup"><span data-stu-id="9d74d-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="9d74d-120">Isso faz com que o armazenamento de mensagens a serem listados na tabela de repositório de mensagens, que está disponível aos clientes através do método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) e para ser aberto sem a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d74d-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="9d74d-121">Se o sinalizador MDB_TEMPORARY estiver definido, MAPI não faz nada e o método retornará imediatamente com S_OK.</span><span class="sxs-lookup"><span data-stu-id="9d74d-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d74d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d74d-122">See also</span></span>



[<span data-ttu-id="9d74d-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="9d74d-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="9d74d-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d74d-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

