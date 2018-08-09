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
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767088"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="eabcc-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="eabcc-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="eabcc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eabcc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eabcc-105">Retorna o repositório de mensagem que contém a mensagem atual, se existir um repositório tal.</span><span class="sxs-lookup"><span data-stu-id="eabcc-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="eabcc-106">Este método retornará NULL no parâmetro _ppStore_ mensagens incorporado, o que são armazenados em outra mensagem em vez de diretamente em um repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="eabcc-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="eabcc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eabcc-107">Parameters</span></span>

 <span data-ttu-id="eabcc-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="eabcc-108">_ppStore_</span></span>
  
> <span data-ttu-id="eabcc-109">[out] Um ponteiro para um ponteiro para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="eabcc-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eabcc-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="eabcc-110">Return value</span></span>

<span data-ttu-id="eabcc-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="eabcc-111">S_OK</span></span> 
  
> <span data-ttu-id="eabcc-112">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="eabcc-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eabcc-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="eabcc-113">S_FALSE</span></span> 
  
> <span data-ttu-id="eabcc-114">Não há nenhum repositório que contém a mensagem.</span><span class="sxs-lookup"><span data-stu-id="eabcc-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eabcc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="eabcc-115">Remarks</span></span>

<span data-ttu-id="eabcc-116">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="eabcc-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eabcc-117">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="eabcc-117">MFCMAPI reference</span></span>

<span data-ttu-id="eabcc-118">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eabcc-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eabcc-119">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="eabcc-119">**File**</span></span>|<span data-ttu-id="eabcc-120">**Function**</span><span class="sxs-lookup"><span data-stu-id="eabcc-120">**Function**</span></span>|<span data-ttu-id="eabcc-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="eabcc-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eabcc-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="eabcc-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="eabcc-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="eabcc-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="eabcc-124">MFCMAPI usa o método **IMAPIMessageSite::GetStore** para obter o ponteiro atualmente em cache para o repositório especificado, se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="eabcc-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eabcc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="eabcc-125">See also</span></span>



[<span data-ttu-id="eabcc-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eabcc-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="eabcc-127">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="eabcc-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="eabcc-128">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="eabcc-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

