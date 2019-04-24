---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338308"
---
# <a name="dtblbutton"></a><span data-ttu-id="9beb0-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="9beb0-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="9beb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9beb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9beb0-105">Contém informações sobre um controle de botão para uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="9beb0-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9beb0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9beb0-106">Header file:</span></span>  <br/> |<span data-ttu-id="9beb0-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9beb0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9beb0-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="9beb0-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="9beb0-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="9beb0-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="9beb0-110">Members</span><span class="sxs-lookup"><span data-stu-id="9beb0-110">Members</span></span>

 <span data-ttu-id="9beb0-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="9beb0-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="9beb0-112">Posição na memória da cadeia de caracteres que é exibida no botão.</span><span class="sxs-lookup"><span data-stu-id="9beb0-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="9beb0-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9beb0-113">**ulFlags**</span></span>
  
> <span data-ttu-id="9beb0-114">Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="9beb0-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="9beb0-115">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9beb0-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="9beb0-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9beb0-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9beb0-117">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9beb0-117">The label is in Unicode format.</span></span> <span data-ttu-id="9beb0-118">Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9beb0-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="9beb0-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="9beb0-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="9beb0-120">Marca de propriedade de uma propriedade do tipo PT_OBJECT que implementa a interface [IMAPIControl](imapicontroliunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="9beb0-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="9beb0-121">Quando o botão é clicado, MAPI chama o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) da implementação [IMAPIProp](imapipropiunknown.md) da tabela de exibição para recuperar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9beb0-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9beb0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9beb0-122">Remarks</span></span>

<span data-ttu-id="9beb0-123">Uma estrutura **DTBLBUTTON** descreve um botão com um controle que, quando clicado, permite que um usuário inicie uma operação.</span><span class="sxs-lookup"><span data-stu-id="9beb0-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="9beb0-124">Normalmente, clicar em um botão faz com que uma caixa de diálogo modal seja exibida ou uma tarefa programática seja invocada.</span><span class="sxs-lookup"><span data-stu-id="9beb0-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="9beb0-125">Os provedores de serviços podem implementar qualquer coisa por meio de um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="9beb0-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="9beb0-126">Se o botão deve executar uma tarefa com base nos valores de outros controles, esses controles devem ter definido o sinalizador DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="9beb0-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="9beb0-127">O membro **ulbLpszLabel** é a posição na memória da cadeia de caracteres que é exibida no botão.</span><span class="sxs-lookup"><span data-stu-id="9beb0-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="9beb0-128">Os provedores de serviços podem adicionar um caractere&amp;de e comercial () para indicar um aceleraDor do Windows no rótulo do botão.</span><span class="sxs-lookup"><span data-stu-id="9beb0-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="9beb0-129">O pressionamento de uma tecla de aceleração tem o mesmo efeito que clicar no botão.</span><span class="sxs-lookup"><span data-stu-id="9beb0-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="9beb0-130">O membro **ulPRControl** descreve uma propriedade de objeto que, quando aberta com o método **IMAPIProp:: OpenProperty** , retorna um ponteiro para um objeto Control.</span><span class="sxs-lookup"><span data-stu-id="9beb0-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="9beb0-131">A implementação de um objeto Control que oferece suporte à interface **IMAPIControl** é uma maneira de estender o conjunto de recursos MAPI e definir a operação ou tarefa que ocorre quando o botão é clicado.</span><span class="sxs-lookup"><span data-stu-id="9beb0-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="9beb0-132">O **IMAPIControl** fornece dois métodos para manipular botões: [GetState](imapicontrol-getstate.md) para desabilitar ou Habilitar botões e [Ativar](imapicontrol-activate.md) para lidar com cliques de botão.</span><span class="sxs-lookup"><span data-stu-id="9beb0-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="9beb0-133">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9beb0-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="9beb0-134">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9beb0-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9beb0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9beb0-135">See also</span></span>



[<span data-ttu-id="9beb0-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="9beb0-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="9beb0-137">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9beb0-137">MAPI Structures</span></span>](mapi-structures.md)

