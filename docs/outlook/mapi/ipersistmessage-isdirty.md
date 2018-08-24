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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576201"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="3737b-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="3737b-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="3737b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3737b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3737b-105">Verifica o formulário para que as alterações feitas desde o último salvamento.</span><span class="sxs-lookup"><span data-stu-id="3737b-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="3737b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3737b-106">Parameters</span></span>

<span data-ttu-id="3737b-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3737b-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3737b-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3737b-108">Return value</span></span>

<span data-ttu-id="3737b-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3737b-109">S_OK</span></span> 
  
> <span data-ttu-id="3737b-110">O formulário tem alterações feitas desde que foi salvo pela última vez.</span><span class="sxs-lookup"><span data-stu-id="3737b-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="3737b-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3737b-111">S_FALSE</span></span> 
  
> <span data-ttu-id="3737b-112">O formulário não terá as alterações feitas desde que foi salvo pela última vez.</span><span class="sxs-lookup"><span data-stu-id="3737b-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3737b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3737b-113">Remarks</span></span>

<span data-ttu-id="3737b-114">Visualizadores de formulário chame o método de **IPersistMessage::IsDirty** para determinar se a mensagem tem os dados.</span><span class="sxs-lookup"><span data-stu-id="3737b-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3737b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="3737b-115">See also</span></span>



[<span data-ttu-id="3737b-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3737b-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

