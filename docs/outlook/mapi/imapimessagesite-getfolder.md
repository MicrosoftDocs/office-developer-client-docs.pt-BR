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
ms.openlocfilehash: 78fb610c5afc3cac4f6de84240f734e5ae196110
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565540"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="b1fa8-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="b1fa8-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="b1fa8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1fa8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1fa8-105">Retorna a pasta na qual a mensagem atual foi criada ou aberta, se existir uma pasta tal.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="b1fa8-106">Este método retornará NULL no parâmetro _ppFolder_ mensagens incorporado, o que não são armazenadas diretamente em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="b1fa8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1fa8-107">Parameters</span></span>

 <span data-ttu-id="b1fa8-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="b1fa8-108">_ppFolder_</span></span>
  
> <span data-ttu-id="b1fa8-109">[out] Um ponteiro para um ponteiro para a pasta retornado.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1fa8-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b1fa8-110">Return value</span></span>

<span data-ttu-id="b1fa8-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1fa8-111">S_OK</span></span> 
  
> <span data-ttu-id="b1fa8-112">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b1fa8-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b1fa8-113">S_FALSE</span></span> 
  
> <span data-ttu-id="b1fa8-114">Nenhuma pasta existe para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1fa8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1fa8-115">Remarks</span></span>

<span data-ttu-id="b1fa8-116">Para obter uma lista das interfaces que estão relacionados aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b1fa8-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b1fa8-117">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b1fa8-117">MFCMAPI reference</span></span>

<span data-ttu-id="b1fa8-118">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b1fa8-119">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b1fa8-119">**File**</span></span>|<span data-ttu-id="b1fa8-120">**Function**</span><span class="sxs-lookup"><span data-stu-id="b1fa8-120">**Function**</span></span>|<span data-ttu-id="b1fa8-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b1fa8-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b1fa8-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b1fa8-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b1fa8-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="b1fa8-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="b1fa8-124">MFCMAPI usa o método **IMAPIMessageSite::GetFolder** para retornar o ponteiro atualmente em cache para a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="b1fa8-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1fa8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1fa8-125">See also</span></span>



[<span data-ttu-id="b1fa8-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1fa8-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="b1fa8-127">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b1fa8-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b1fa8-128">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="b1fa8-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

