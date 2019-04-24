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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309615"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="41927-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="41927-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="41927-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41927-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41927-105">Salva um formulário revisado de volta para a mensagem a partir da qual foi carregado ou criado.</span><span class="sxs-lookup"><span data-stu-id="41927-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="41927-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41927-106">Parameters</span></span>

 <span data-ttu-id="41927-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="41927-107">_pMessage_</span></span>
  
> <span data-ttu-id="41927-108">no Um ponteiro para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="41927-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="41927-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="41927-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="41927-110">no TRUE para indicar que a mensagem indicada por _PMessage_ é a mensagem a partir da qual o formulário foi carregado ou criado; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="41927-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41927-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="41927-111">Return value</span></span>

<span data-ttu-id="41927-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="41927-112">S_OK</span></span> 
  
> <span data-ttu-id="41927-113">O formulário foi salvo com êxito.</span><span class="sxs-lookup"><span data-stu-id="41927-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41927-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="41927-114">Remarks</span></span>

<span data-ttu-id="41927-115">Os visualizadores de formulários chamam o método **IPersistMessage:: Save** para salvar um formulário revisado de volta para a mensagem a partir da qual foi carregado ou criado.</span><span class="sxs-lookup"><span data-stu-id="41927-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="41927-116">**Save** só deve ser chamado quando o formulário estiver em seu estado [normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="41927-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="41927-117">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="41927-117">Notes to implementers</span></span>

<span data-ttu-id="41927-118">Não confirmar as alterações salvas; o chamador deve confirmar as alterações.</span><span class="sxs-lookup"><span data-stu-id="41927-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="41927-119">Nunca faça alterações nas propriedades que pertencem à mensagem do formulário, exceto durante a chamada de **salvamento** .</span><span class="sxs-lookup"><span data-stu-id="41927-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="41927-120">Se _fSameAsLoad_ estiver definido como true, você poderá salvar as alterações na mensagem existente do formulário.</span><span class="sxs-lookup"><span data-stu-id="41927-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="41927-121">Se _fSameAsLoad_ estiver definido como false, você deverá copiar todas as propriedades da mensagem original para a mensagem indicada por _PMessage_ antes de executar Save.</span><span class="sxs-lookup"><span data-stu-id="41927-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="41927-122">Use o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da mensagem original para copiar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="41927-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="41927-123">Quando todas as propriedades tiverem sido copiadas, insira [](noscribble-state.md) o estado norabisco.</span><span class="sxs-lookup"><span data-stu-id="41927-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="41927-124">Se nenhum erro ocorrer, retorne S_OK.</span><span class="sxs-lookup"><span data-stu-id="41927-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="41927-125">Caso contrário, retorne o erro da ação com falha.</span><span class="sxs-lookup"><span data-stu-id="41927-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="41927-126">Se **Save** for chamado quando o formulário estiver em qualquer estado diferente de normal, retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="41927-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="41927-127">Para obter mais informações sobre como salvar objetos de armazenamento, consulte a documentação nos métodos [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="41927-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41927-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="41927-128">See also</span></span>



[<span data-ttu-id="41927-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41927-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="41927-130">Estados de formulário</span><span class="sxs-lookup"><span data-stu-id="41927-130">Form States</span></span>](form-states.md)

