---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767601"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="0c19c-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="0c19c-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="0c19c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c19c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c19c-105">Retorna um identificador que representa o servidor de formulário que pode gerenciar o formulário.</span><span class="sxs-lookup"><span data-stu-id="0c19c-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="0c19c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c19c-106">Parameters</span></span>

 <span data-ttu-id="0c19c-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="0c19c-107">_lpClassID_</span></span>
  
> <span data-ttu-id="0c19c-108">[além, out] Um ponteiro para o identificador de classe (CLSID) do formulário.</span><span class="sxs-lookup"><span data-stu-id="0c19c-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c19c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0c19c-109">Return value</span></span>

<span data-ttu-id="0c19c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c19c-110">S_OK</span></span> 
  
> <span data-ttu-id="0c19c-111">O identificador de classe foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="0c19c-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c19c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c19c-112">Remarks</span></span>

<span data-ttu-id="0c19c-113">O método **IPersistMessge::GetClassID** define o conteúdo do parâmetro _lpClassID_ como identificador de classe do servidor formulário e retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="0c19c-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="0c19c-114">Quando um visualizador de formulário chama **GetClassID** e ela retorna com êxito, o formulário é colocado no estado [não inicializado](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="0c19c-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="0c19c-115">Para obter mais informações sobre como os identificadores de classe são usados com os objetos de armazenamento estruturado, consulte a documentação para o método [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0c19c-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c19c-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c19c-116">See also</span></span>



[<span data-ttu-id="0c19c-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c19c-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

