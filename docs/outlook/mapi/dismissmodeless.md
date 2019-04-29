---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428183"
---
# <a name="dismissmodeless"></a><span data-ttu-id="80ed7-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="80ed7-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="80ed7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80ed7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80ed7-105">Define uma função de retorno de chamada que MAPI chama quando ele desrecebeu uma caixa de diálogo do catálogo de endereços sem restrições.</span><span class="sxs-lookup"><span data-stu-id="80ed7-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80ed7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="80ed7-106">Header file:</span></span>  <br/> |<span data-ttu-id="80ed7-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="80ed7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="80ed7-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="80ed7-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="80ed7-109">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="80ed7-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="80ed7-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="80ed7-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="80ed7-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="80ed7-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="80ed7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80ed7-112">Parameters</span></span>

 <span data-ttu-id="80ed7-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="80ed7-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="80ed7-114">no Um valor específico da implementação normalmente usado para passar informações da interface do usuário para uma função.</span><span class="sxs-lookup"><span data-stu-id="80ed7-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="80ed7-115">Por exemplo, no Microsoft Windows, esse parâmetro é o identificador de janela pai da caixa de diálogo e é do tipo HWND, CAST para um **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="80ed7-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="80ed7-116">Um valor igual A zero indica que não há janela pai.</span><span class="sxs-lookup"><span data-stu-id="80ed7-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="80ed7-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="80ed7-117">_lpvContext_</span></span>
  
> <span data-ttu-id="80ed7-118">no Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando MAPI o chama.</span><span class="sxs-lookup"><span data-stu-id="80ed7-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="80ed7-119">Esse valor pode representar um endereço de importância para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="80ed7-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="80ed7-120">Normalmente, para o código C++, _lpvContext_ é um ponteiro para o endereço de uma instância de objeto do C++.</span><span class="sxs-lookup"><span data-stu-id="80ed7-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="80ed7-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="80ed7-121">Return value</span></span>

<span data-ttu-id="80ed7-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="80ed7-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80ed7-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="80ed7-123">Remarks</span></span>

<span data-ttu-id="80ed7-124">Quando o aplicativo cliente invoca uma caixa de diálogo do catálogo de endereços sem restrições, ele inclui em seu loop de mensagem do Windows uma chamada para uma função com base no protótipo [ACCELERATEABSDI](accelerateabsdi.md) , que verifica e processa teclas de aceleração.</span><span class="sxs-lookup"><span data-stu-id="80ed7-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="80ed7-125">Quando a caixa de diálogo é fechada, MAPI chama a função baseada em **DISMISSMODELESS** para que o aplicativo cliente pare de chamar a função baseada em **ACCELERATEABSDI** .</span><span class="sxs-lookup"><span data-stu-id="80ed7-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80ed7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="80ed7-126">See also</span></span>



[<span data-ttu-id="80ed7-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="80ed7-127">ADRPARM</span></span>](adrparm.md)

