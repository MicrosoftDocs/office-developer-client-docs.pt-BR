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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309622"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="40a81-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="40a81-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="40a81-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40a81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40a81-105">Retorna um identificador que representa o servidor de formulário que pode gerenciar o formulário.</span><span class="sxs-lookup"><span data-stu-id="40a81-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="40a81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40a81-106">Parameters</span></span>

 <span data-ttu-id="40a81-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="40a81-107">_lpClassID_</span></span>
  
> <span data-ttu-id="40a81-108">[in, out] Um ponteiro para o identificador de classe (CLSID) do formulário.</span><span class="sxs-lookup"><span data-stu-id="40a81-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40a81-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="40a81-109">Return value</span></span>

<span data-ttu-id="40a81-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="40a81-110">S_OK</span></span> 
  
> <span data-ttu-id="40a81-111">O identificador de classe foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="40a81-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40a81-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="40a81-112">Remarks</span></span>

<span data-ttu-id="40a81-113">O método **IPersistMessge::** GetClassID define o conteúdo do parâmetro _lpClassID_ para o identificador de classe do servidor de formulário e retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="40a81-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="40a81-114">Quando um visualizador de formulários \*\*\*\* chama GetClassID e retorna com êxito, o formulário é colocado no estado [](uninitialized-state.md) Uninitialized.</span><span class="sxs-lookup"><span data-stu-id="40a81-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="40a81-115">Para obter mais informações sobre como os identificadores de classe são usados com objetos de armazenamento estruturados, consulte a documentação do método [IPersist::](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) GetClassID.</span><span class="sxs-lookup"><span data-stu-id="40a81-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40a81-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="40a81-116">See also</span></span>



[<span data-ttu-id="40a81-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40a81-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

