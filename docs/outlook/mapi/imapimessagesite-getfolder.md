---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321382"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="1e17e-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="1e17e-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="1e17e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e17e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e17e-105">Retorna a pasta na qual a mensagem atual foi criada ou aberta, se essa pasta existir.</span><span class="sxs-lookup"><span data-stu-id="1e17e-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="1e17e-106">Este método retorna NULL no parâmetro _ppFolder_ para mensagens incorporadas, que não são armazenadas diretamente em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1e17e-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="1e17e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e17e-107">Parameters</span></span>

 <span data-ttu-id="1e17e-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="1e17e-108">_ppFolder_</span></span>
  
> <span data-ttu-id="1e17e-109">bota Um ponteiro para um ponteiro para a pasta retornada.</span><span class="sxs-lookup"><span data-stu-id="1e17e-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e17e-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1e17e-110">Return value</span></span>

<span data-ttu-id="1e17e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e17e-111">S_OK</span></span> 
  
> <span data-ttu-id="1e17e-112">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1e17e-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1e17e-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1e17e-113">S_FALSE</span></span> 
  
> <span data-ttu-id="1e17e-114">Nenhuma pasta existe para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1e17e-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e17e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e17e-115">Remarks</span></span>

<span data-ttu-id="1e17e-116">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulários MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="1e17e-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1e17e-117">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1e17e-117">MFCMAPI reference</span></span>

<span data-ttu-id="1e17e-118">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e17e-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1e17e-119">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1e17e-119">**File**</span></span>|<span data-ttu-id="1e17e-120">**Função**</span><span class="sxs-lookup"><span data-stu-id="1e17e-120">**Function**</span></span>|<span data-ttu-id="1e17e-121">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1e17e-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e17e-122">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="1e17e-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1e17e-123">CMyMAPIFormViewer:: getFolder</span><span class="sxs-lookup"><span data-stu-id="1e17e-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="1e17e-124">MFCMAPI usa o método **IMAPIMessageSite:: GetFolder** para retornar o ponteiro em cache atualmente para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="1e17e-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e17e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e17e-125">See also</span></span>



[<span data-ttu-id="1e17e-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e17e-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="1e17e-127">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1e17e-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1e17e-128">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="1e17e-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

