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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316593"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="0ecc3-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="0ecc3-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="0ecc3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ecc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ecc3-105">Faz alterações em uma seção de perfil do repositório de mensagens permanente.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0ecc3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ecc3-106">Parameters</span></span>

 <span data-ttu-id="0ecc3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ecc3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0ecc3-108">no Uma bitmask de sinalizadores que indica o tipo de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="0ecc3-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="0ecc3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0ecc3-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="0ecc3-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="0ecc3-111">O repositório de mensagens é temporário e não deve ser adicionado à tabela do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="0ecc3-112">Quando MDB_TEMPORARY é definido, **ModifyProfile** retorna S_OK imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0ecc3-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0ecc3-113">Return value</span></span>

<span data-ttu-id="0ecc3-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ecc3-114">S_OK</span></span> 
  
> <span data-ttu-id="0ecc3-115">As alterações na seção de perfil foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ecc3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ecc3-116">Remarks</span></span>

<span data-ttu-id="0ecc3-117">O método **IMAPISupport:: ModifyProfile** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="0ecc3-118">Os provedores de repositório de mensagens chamam o **ModifyProfile** para solicitar que o MAPI modifique suas informações de perfil.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="0ecc3-119">**ModifyProfile** adiciona a seção de perfil associada ao provedor de chamadas à lista de recursos do provedor de repositório de mensagens instalado.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="0ecc3-120">Isso faz com que o repositório de mensagens seja listado na tabela do repositório de mensagens, que está disponível para clientes por meio do método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) , e a ser aberto sem a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="0ecc3-121">Se o sinalizador MDB_TEMPORARY for definido, MAPI não fará nada e o método retornará imediatamente com S_OK.</span><span class="sxs-lookup"><span data-stu-id="0ecc3-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ecc3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ecc3-122">See also</span></span>



[<span data-ttu-id="0ecc3-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="0ecc3-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="0ecc3-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ecc3-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

