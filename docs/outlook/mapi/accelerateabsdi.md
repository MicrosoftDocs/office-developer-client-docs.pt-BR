---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322124"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="c47a4-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="c47a4-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="c47a4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c47a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c47a4-105">Define uma função de retorno de chamada para processar teclas de aceleração em uma caixa de diálogo do catálogo de endereços sem restrições.</span><span class="sxs-lookup"><span data-stu-id="c47a4-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c47a4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c47a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="c47a4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c47a4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c47a4-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="c47a4-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c47a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c47a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c47a4-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="c47a4-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c47a4-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c47a4-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="c47a4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c47a4-112">Parameters</span></span>

 <span data-ttu-id="c47a4-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c47a4-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="c47a4-114">no Um valor específico de implementação usado para passar informações da interface do usuário para uma função.</span><span class="sxs-lookup"><span data-stu-id="c47a4-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="c47a4-115">Em aplicativos executados no Microsoft Windows, _ulUIParam_ é o identificador da janela pai de uma caixa de diálogo e é do tipo HWND, CAST para um **ULONG_PTR**.</span><span class="sxs-lookup"><span data-stu-id="c47a4-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="c47a4-116">Um valor igual A zero indica que não há janela pai.</span><span class="sxs-lookup"><span data-stu-id="c47a4-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="c47a4-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="c47a4-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="c47a4-118">no Ponteiro para uma mensagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="c47a4-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c47a4-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c47a4-119">Return value</span></span>

<span data-ttu-id="c47a4-120">Uma função com o protótipo **ACCELERATEABSDI** retorna true se ele lida com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c47a4-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c47a4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c47a4-121">Remarks</span></span>

<span data-ttu-id="c47a4-122">Uma função com base no protótipo **ACCELERATEABSDI** é usada apenas com uma caixa de diálogo sem janela restrita, ou seja, somente se o aplicativo cliente tiver definido o sinalizador DIALOG_SDI no membro _Parâmetroulflags_ da estrutura [ADRPARM](adrparm.md) .</span><span class="sxs-lookup"><span data-stu-id="c47a4-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="c47a4-123">Uma caixa de diálogo sem janela restrita compartilha o loop de mensagem do Windows do aplicativo cliente, em vez de ter seu próprio loop.</span><span class="sxs-lookup"><span data-stu-id="c47a4-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="c47a4-124">O aplicativo, que controla o loop de mensagem, não sabe quais teclas de aceleração a caixa de diálogo usa, portanto, ele chama uma função baseada em **ACCELERATEABSDI** para testar e agir em teclas de aceleração, como CTRL + P para impressão.</span><span class="sxs-lookup"><span data-stu-id="c47a4-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="c47a4-125">O loop de mensagens de um cliente chama a função baseada em **ACCELERATEABSDI** quando o cliente invoca uma caixa de diálogo do catálogo de endereços sem restrições com o método de [endereço IAddrBook::](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="c47a4-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="c47a4-126">Essa chamada é terminada quando MAPI chama uma função com base no protótipo de função [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="c47a4-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

