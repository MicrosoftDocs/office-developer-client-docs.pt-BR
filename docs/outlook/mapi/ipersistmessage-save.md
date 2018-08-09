---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 222d8257a802739ee8e513a0ea95a13f4b99322e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767605"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="084c5-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="084c5-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="084c5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="084c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="084c5-105">Salva um formulário revisado na mensagem do qual ele foi carregado ou criado.</span><span class="sxs-lookup"><span data-stu-id="084c5-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="084c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="084c5-106">Parameters</span></span>

 <span data-ttu-id="084c5-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="084c5-107">_pMessage_</span></span>
  
> <span data-ttu-id="084c5-108">[in] Um ponteiro para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="084c5-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="084c5-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="084c5-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="084c5-110">[in] TRUE para indicar que a mensagem apontado por _pMessage_ é a mensagem a partir do qual o formulário foi carregado ou criado; Caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="084c5-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="084c5-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="084c5-111">Return value</span></span>

<span data-ttu-id="084c5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="084c5-112">S_OK</span></span> 
  
> <span data-ttu-id="084c5-113">O formulário foi salvo com êxito.</span><span class="sxs-lookup"><span data-stu-id="084c5-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="084c5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="084c5-114">Remarks</span></span>

<span data-ttu-id="084c5-115">Visualizadores de formulário chame o método de **IPersistMessage::Save** para salvar um formulário revisado na mensagem do qual ele foi carregado ou criado.</span><span class="sxs-lookup"><span data-stu-id="084c5-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="084c5-116">**Salvar** só deve ser chamado quando o formulário está em seu estado [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="084c5-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="084c5-117">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="084c5-117">Notes to implementers</span></span>

<span data-ttu-id="084c5-118">Não confirmar as alterações salvas; é até o chamador para confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="084c5-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="084c5-119">Nunca fazer alterações nas propriedades que pertencem a mensagem do formulário, exceto durante a chamada de **Salvar** .</span><span class="sxs-lookup"><span data-stu-id="084c5-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="084c5-120">Se _fSameAsLoad_ for definido como TRUE, você pode salvar as alterações de mensagem existente do formulário.</span><span class="sxs-lookup"><span data-stu-id="084c5-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="084c5-121">Se _fSameAsLoad_ estiver definida como FALSE, você deve copiar todas as propriedades da mensagem original na mensagem apontada pela _pMessage_ antes de salvar.</span><span class="sxs-lookup"><span data-stu-id="084c5-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="084c5-122">Use o método de [IMAPIProp::CopyTo](imapiprop-copyto.md) da mensagem original para copiar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="084c5-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="084c5-123">Quando tiverem sido copiadas todas as propriedades, insira o estado de [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="084c5-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="084c5-124">Se nenhum erro ocorrer, retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="084c5-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="084c5-125">Caso contrário, retornará o erro da ação com falha.</span><span class="sxs-lookup"><span data-stu-id="084c5-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="084c5-126">Se **Salvar** é chamado quando o formulário estiver em qualquer estado que não seja Normal, retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="084c5-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="084c5-127">Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação sobre os métodos [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="084c5-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="084c5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="084c5-128">See also</span></span>



[<span data-ttu-id="084c5-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="084c5-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="084c5-130">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="084c5-130">Form States</span></span>](form-states.md)

