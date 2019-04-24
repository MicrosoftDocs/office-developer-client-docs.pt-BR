---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309608"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="759f4-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="759f4-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="759f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="759f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="759f4-105">Verifica se há alterações feitas desde o último salvamento no formulário.</span><span class="sxs-lookup"><span data-stu-id="759f4-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="759f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="759f4-106">Parameters</span></span>

<span data-ttu-id="759f4-107">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="759f4-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="759f4-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="759f4-108">Return value</span></span>

<span data-ttu-id="759f4-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="759f4-109">S_OK</span></span> 
  
> <span data-ttu-id="759f4-110">O formulário tem alterações feitas desde que foi salvo pela última vez.</span><span class="sxs-lookup"><span data-stu-id="759f4-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="759f4-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="759f4-111">S_FALSE</span></span> 
  
> <span data-ttu-id="759f4-112">O formulário não tem alterações feitas desde que foi salvo pela última vez.</span><span class="sxs-lookup"><span data-stu-id="759f4-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="759f4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="759f4-113">Remarks</span></span>

<span data-ttu-id="759f4-114">Os visualizadores de formulários chamam o método **IPersistMessage:: IsDirty** para determinar se a mensagem tem dados não salvos.</span><span class="sxs-lookup"><span data-stu-id="759f4-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="759f4-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="759f4-115">See also</span></span>



[<span data-ttu-id="759f4-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="759f4-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

