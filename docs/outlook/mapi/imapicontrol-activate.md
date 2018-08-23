---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580681"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="60eec-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="60eec-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="60eec-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60eec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60eec-105">Executa uma tarefa como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário do aplicativo cliente clica no controle de botão.</span><span class="sxs-lookup"><span data-stu-id="60eec-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="60eec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60eec-106">Parameters</span></span>

 <span data-ttu-id="60eec-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60eec-107">_ulFlags_</span></span>
  
> <span data-ttu-id="60eec-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="60eec-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="60eec-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="60eec-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="60eec-110">[in] Uma alça para a janela pai da caixa de diálogo na qual o controle de botão aparece.</span><span class="sxs-lookup"><span data-stu-id="60eec-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60eec-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="60eec-111">Return value</span></span>

<span data-ttu-id="60eec-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="60eec-112">S_OK</span></span> 
  
> <span data-ttu-id="60eec-113">O controle de botão foi ativado com êxito.</span><span class="sxs-lookup"><span data-stu-id="60eec-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60eec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="60eec-114">Remarks</span></span>

<span data-ttu-id="60eec-115">O método **IMAPIControl::Activate** executa tarefas após o clique de um usuário do controle de botão.</span><span class="sxs-lookup"><span data-stu-id="60eec-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="60eec-116">Após o clique ocorre, como parte do processamento da tabela exibição, o MAPI faz uma chamada para **Ativar** após a primeira chamada [IMAPIControl::GetState](imapicontrol-getstate.md) para determinar se o botão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="60eec-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="60eec-117">Para obter mais informações sobre como implementar **Ativar** e o outro [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, consulte a [Implementação do objeto de controle](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="60eec-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60eec-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="60eec-118">See also</span></span>



[<span data-ttu-id="60eec-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="60eec-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="60eec-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60eec-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

