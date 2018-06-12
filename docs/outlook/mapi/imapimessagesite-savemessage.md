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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ec85f7bdfc9d2d275bdb5ffe7ba0113ad4a35c3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767097"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="1ed5e-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="1ed5e-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="1ed5e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ed5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ed5e-105">Solicita que a mensagem atual seja salvo.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="1ed5e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ed5e-106">Parameters</span></span>

<span data-ttu-id="1ed5e-107">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1ed5e-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1ed5e-108">Return value</span></span>

<span data-ttu-id="1ed5e-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ed5e-109">S_OK</span></span> 
  
> <span data-ttu-id="1ed5e-110">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1ed5e-111">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="1ed5e-111">Remarks</span></span>

<span data-ttu-id="1ed5e-112">Formulários chame o método de **IMAPIMessageSite::SaveMessage** para solicitar que uma mensagem seja salvo.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="1ed5e-113">Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="1ed5e-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ed5e-114">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1ed5e-114">MFCMAPI reference</span></span>

<span data-ttu-id="1ed5e-115">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ed5e-116">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1ed5e-116">**File**</span></span>|<span data-ttu-id="1ed5e-117">**Function**</span><span class="sxs-lookup"><span data-stu-id="1ed5e-117">**Function**</span></span>|<span data-ttu-id="1ed5e-118">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1ed5e-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ed5e-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="1ed5e-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1ed5e-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="1ed5e-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="1ed5e-121">MFCMAPI usa o método **IMAPIMessageSite::SaveMessage** para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ed5e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ed5e-122">See also</span></span>



[<span data-ttu-id="1ed5e-123">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ed5e-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="1ed5e-124">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1ed5e-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1ed5e-125">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="1ed5e-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

