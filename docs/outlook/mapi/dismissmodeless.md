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
# <a name="dismissmodeless"></a><span data-ttu-id="8bd62-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="8bd62-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="8bd62-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bd62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bd62-105">Define uma função de retorno de chamada que MAPI chama quando descarta uma caixa de diálogo de agenda sem modo.</span><span class="sxs-lookup"><span data-stu-id="8bd62-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bd62-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8bd62-106">Header file:</span></span>  <br/> |<span data-ttu-id="8bd62-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bd62-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8bd62-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="8bd62-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="8bd62-109">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="8bd62-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="8bd62-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="8bd62-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="8bd62-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="8bd62-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="8bd62-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bd62-112">Parameters</span></span>

 <span data-ttu-id="8bd62-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8bd62-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="8bd62-114">[in] Um valor específico de implementação normalmente usado para passar informações da interface do usuário para uma função.</span><span class="sxs-lookup"><span data-stu-id="8bd62-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="8bd62-115">Por exemplo, no Microsoft Windows esse parâmetro é o identificador da janela pai da caixa de diálogo e é do tipo HWND, cast em um **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="8bd62-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="8bd62-116">Um valor zero indica que não há janela pai.</span><span class="sxs-lookup"><span data-stu-id="8bd62-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="8bd62-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="8bd62-117">_lpvContext_</span></span>
  
> <span data-ttu-id="8bd62-118">[in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando MAPI o chama.</span><span class="sxs-lookup"><span data-stu-id="8bd62-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="8bd62-119">Esse valor pode representar um endereço significativo para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="8bd62-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="8bd62-120">Normalmente, para código C++,  _lpvContext_ é um ponteiro para o endereço de uma instância de objeto C++.</span><span class="sxs-lookup"><span data-stu-id="8bd62-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8bd62-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8bd62-121">Return value</span></span>

<span data-ttu-id="8bd62-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8bd62-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bd62-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bd62-123">Remarks</span></span>

<span data-ttu-id="8bd62-124">Quando o aplicativo cliente invoca uma caixa de diálogo de livro de endereços sem janelas, ele inclui em seu loop de mensagem do Windows uma chamada para uma função com base no protótipo [ACCELERATEABSDI,](accelerateabsdi.md) que verifica e processa teclas aceleradoras.</span><span class="sxs-lookup"><span data-stu-id="8bd62-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="8bd62-125">Quando a caixa de diálogo é fechada, MAPI chama a função baseada **DISMISSMODELESS** para que o aplicativo cliente pare de chamar a **função baseada ACCELERATEABSDI.**</span><span class="sxs-lookup"><span data-stu-id="8bd62-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8bd62-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bd62-126">See also</span></span>



[<span data-ttu-id="8bd62-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="8bd62-127">ADRPARM</span></span>](adrparm.md)

