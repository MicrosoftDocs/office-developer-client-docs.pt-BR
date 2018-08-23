---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567388"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="24a6b-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="24a6b-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="24a6b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24a6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24a6b-105">Diminui a contagem de referência, limpa e exclui por instância dados globais para a DLL de MAPI.</span><span class="sxs-lookup"><span data-stu-id="24a6b-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24a6b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="24a6b-106">Header file:</span></span>  <br/> |<span data-ttu-id="24a6b-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="24a6b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="24a6b-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="24a6b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="24a6b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="24a6b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="24a6b-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="24a6b-110">Called by:</span></span>  <br/> |<span data-ttu-id="24a6b-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="24a6b-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="24a6b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24a6b-112">Parameters</span></span>

<span data-ttu-id="24a6b-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="24a6b-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="24a6b-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="24a6b-114">Return value</span></span>

<span data-ttu-id="24a6b-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="24a6b-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24a6b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="24a6b-116">Remarks</span></span>

<span data-ttu-id="24a6b-117">Um aplicativo cliente chama a função **MAPIUninitialize** para encerrar sua interação com MAPI, começado com uma chamada para a função [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="24a6b-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="24a6b-118">Após a chamada **MAPIUninitialize** , nenhuma outra chamada MAPI pode ser feita pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="24a6b-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="24a6b-119">**MAPIUninitialize** diminui a contagem de referência e a função **MAPIInitialize** correspondente incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="24a6b-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="24a6b-120">Assim, o número de chamadas para uma função deve ser igual o número de chamadas para outro.</span><span class="sxs-lookup"><span data-stu-id="24a6b-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="24a6b-121">Você não pode chamar **MAPIInitialize** ou **MAPIUninitialize** de dentro de uma função do Win32 **DllMain** ou qualquer outra função que cria ou finaliza threads.</span><span class="sxs-lookup"><span data-stu-id="24a6b-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="24a6b-122">Para obter mais informações, consulte [Usando objetos de Thread-Safe](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="24a6b-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

