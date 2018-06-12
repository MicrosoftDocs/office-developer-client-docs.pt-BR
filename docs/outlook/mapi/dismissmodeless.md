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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: dc830665f425b747d2fdb05641dc037a2e84f695
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766433"
---
# <a name="dismissmodeless"></a><span data-ttu-id="6ef6b-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="6ef6b-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="6ef6b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ef6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ef6b-105">Define uma função de retorno de chamada que chamadas MAPI quando ele tem descartado uma caixa de diálogo do catálogo de endereços sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ef6b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6ef6b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ef6b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ef6b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6ef6b-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="6ef6b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="6ef6b-109">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="6ef6b-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="6ef6b-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="6ef6b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="6ef6b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ef6b-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="6ef6b-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6ef6b-112">Parameters</span></span>

 <span data-ttu-id="6ef6b-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6ef6b-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6ef6b-114">[in] Um valor específico de implementação que geralmente é usado para passar informações de interface de usuário para uma função.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="6ef6b-115">Por exemplo, no Microsoft Windows esse parâmetro é o identificador da janela pai para a caixa de diálogo e é do tipo HWND, convertida em um **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="6ef6b-116">Um valor de zero indica que não há nenhuma janela pai.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="6ef6b-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="6ef6b-117">_lpvContext_</span></span>
  
> <span data-ttu-id="6ef6b-118">[in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando chamadas de MAPI-lo.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="6ef6b-119">Esse valor pode representar um endereço de significância ao aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="6ef6b-120">Geralmente, para código C++, _lpvContext_ é um ponteiro para o endereço de uma instância do objeto C++.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6ef6b-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6ef6b-121">Return value</span></span>

<span data-ttu-id="6ef6b-122">None</span><span class="sxs-lookup"><span data-stu-id="6ef6b-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ef6b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ef6b-123">Remarks</span></span>

<span data-ttu-id="6ef6b-124">Quando o aplicativo cliente invoca uma caixa de diálogo do catálogo de endereços sem janela restrita, ele inclui em seu loop de mensagem do Windows uma chamada para uma função com base em protótipo [ACCELERATEABSDI](accelerateabsdi.md) , que procura e processa as teclas de aceleração.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="6ef6b-125">Quando a caixa de diálogo é fechada, chamadas de MAPI o **DISMISSMODELESS** com base em função para que o aplicativo cliente será interrompida chamando o **ACCELERATEABSDI** com base em função.</span><span class="sxs-lookup"><span data-stu-id="6ef6b-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ef6b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ef6b-126">See also</span></span>



[<span data-ttu-id="6ef6b-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="6ef6b-127">ADRPARM</span></span>](adrparm.md)

