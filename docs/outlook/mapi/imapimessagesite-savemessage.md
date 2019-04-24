---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321417"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="65844-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="65844-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="65844-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65844-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65844-105">Solicita que a mensagem atual seja salva.</span><span class="sxs-lookup"><span data-stu-id="65844-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="65844-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65844-106">Parameters</span></span>

<span data-ttu-id="65844-107">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="65844-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="65844-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="65844-108">Return value</span></span>

<span data-ttu-id="65844-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="65844-109">S_OK</span></span> 
  
> <span data-ttu-id="65844-110">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="65844-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="65844-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="65844-111">Remarks</span></span>

<span data-ttu-id="65844-112">Os formulários chamam o método **IMAPIMessageSite:: SaveMessage** para solicitar que uma mensagem seja salva.</span><span class="sxs-lookup"><span data-stu-id="65844-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="65844-113">Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="65844-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="65844-114">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="65844-114">MFCMAPI reference</span></span>

<span data-ttu-id="65844-115">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="65844-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="65844-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="65844-116">**File**</span></span>|<span data-ttu-id="65844-117">**Função**</span><span class="sxs-lookup"><span data-stu-id="65844-117">**Function**</span></span>|<span data-ttu-id="65844-118">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="65844-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="65844-119">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="65844-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="65844-120">CMyMAPIFormViewer:: SaveMessage</span><span class="sxs-lookup"><span data-stu-id="65844-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="65844-121">MFCMAPI usa o método **IMAPIMessageSite:: SaveMessage** para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="65844-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65844-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="65844-122">See also</span></span>



[<span data-ttu-id="65844-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65844-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="65844-124">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="65844-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="65844-125">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="65844-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

