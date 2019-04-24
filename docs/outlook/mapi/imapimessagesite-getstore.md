---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321431"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="3b8d7-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="3b8d7-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="3b8d7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b8d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b8d7-105">Retorna o repositório de mensagens que contém a mensagem atual, se esse repositório existir.</span><span class="sxs-lookup"><span data-stu-id="3b8d7-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="3b8d7-106">Este método retornará nulo no parâmetro _ppStore_ para mensagens incorporadas, que são armazenadas em outra mensagem em vez de diretamente em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3b8d7-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="3b8d7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b8d7-107">Parameters</span></span>

 <span data-ttu-id="3b8d7-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="3b8d7-108">_ppStore_</span></span>
  
> <span data-ttu-id="3b8d7-109">bota Um ponteiro para um ponteiro para o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3b8d7-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b8d7-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3b8d7-110">Return value</span></span>

<span data-ttu-id="3b8d7-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b8d7-111">S_OK</span></span> 
  
> <span data-ttu-id="3b8d7-112">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="3b8d7-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3b8d7-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3b8d7-113">S_FALSE</span></span> 
  
> <span data-ttu-id="3b8d7-114">Não há um repositório que contenha a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b8d7-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b8d7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b8d7-115">Remarks</span></span>

<span data-ttu-id="3b8d7-116">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="3b8d7-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b8d7-117">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3b8d7-117">MFCMAPI reference</span></span>

<span data-ttu-id="3b8d7-118">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b8d7-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b8d7-119">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="3b8d7-119">**File**</span></span>|<span data-ttu-id="3b8d7-120">**Função**</span><span class="sxs-lookup"><span data-stu-id="3b8d7-120">**Function**</span></span>|<span data-ttu-id="3b8d7-121">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="3b8d7-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b8d7-122">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="3b8d7-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="3b8d7-123">CMyMAPIFormViewer:: getStore</span><span class="sxs-lookup"><span data-stu-id="3b8d7-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="3b8d7-124">MFCMAPI usa o método **IMAPIMessageSite:: GetStore** para obter o ponteiro atualmente em cache para o repositório especificado, se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="3b8d7-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b8d7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b8d7-125">See also</span></span>



[<span data-ttu-id="3b8d7-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b8d7-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="3b8d7-127">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="3b8d7-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="3b8d7-128">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8d7-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

