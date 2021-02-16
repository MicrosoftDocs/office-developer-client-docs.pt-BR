---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338105"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="e6c2c-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="e6c2c-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="e6c2c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6c2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6c2c-105">Encerra uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="e6c2c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6c2c-106">Parameters</span></span>

 <span data-ttu-id="e6c2c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e6c2c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="e6c2c-108">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="e6c2c-109">Esse parâmetro será ignorado se o sinalizador MAPI_LOGOFF_UI não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="e6c2c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6c2c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e6c2c-111">[in] Uma máscara de bits de sinalizadores que controlam a operação de logoff.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="e6c2c-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e6c2c-112">The following flags can be set:</span></span>
    
<span data-ttu-id="e6c2c-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="e6c2c-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="e6c2c-114">Se essa sessão for compartilhada, todos os clientes conectados usando a sessão compartilhada deverão ser notificados sobre o logoff em andamento.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="e6c2c-115">Os clientes devem fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-115">The clients should log off.</span></span> <span data-ttu-id="e6c2c-116">Qualquer cliente que está usando a sessão compartilhada pode definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="e6c2c-117">MAPI_LOGOFF_SHARED será ignorado se a sessão atual não for compartilhada.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="e6c2c-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="e6c2c-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="e6c2c-119">**Logoff** pode exibir uma caixa de diálogo durante a operação, possivelmente solicitando a confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="e6c2c-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="e6c2c-120">_ulReserved_</span></span>
  
> <span data-ttu-id="e6c2c-121">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6c2c-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e6c2c-122">Return value</span></span>

<span data-ttu-id="e6c2c-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6c2c-123">S_OK</span></span> 
  
> <span data-ttu-id="e6c2c-124">A operação de logoff foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6c2c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6c2c-125">Remarks</span></span>

<span data-ttu-id="e6c2c-126">O **método IMAPISession::Logoff** encerra uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="e6c2c-127">Quando **Logoff** retorna, nenhum dos métodos exceto [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6c2c-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e6c2c-128">Notes to callers</span></span>

<span data-ttu-id="e6c2c-129">Quando **Logoff** retornar, libere o objeto session chamando seu **método IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="e6c2c-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="e6c2c-130">Para obter mais informações sobre como encerrar uma sessão, consulte [Terminando uma sessão MAPI](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="e6c2c-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e6c2c-131">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e6c2c-131">MFCMAPI reference</span></span>

<span data-ttu-id="e6c2c-132">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e6c2c-133">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e6c2c-133">**File**</span></span>|<span data-ttu-id="e6c2c-134">**Função**</span><span class="sxs-lookup"><span data-stu-id="e6c2c-134">**Function**</span></span>|<span data-ttu-id="e6c2c-135">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e6c2c-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6c2c-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="e6c2c-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="e6c2c-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="e6c2c-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="e6c2c-138">MFCMAPI usa o **método IMAPISession::Logoff** para fazer logoff da sessão antes de liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e6c2c-139">Devido ao comportamento de desligamento rápido introduzido no Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 e Microsoft Outlook 2013, os clientes nunca devem passar o parâmetro **MAPI_LOGOFF_SHARED** para [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="e6c2c-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="e6c2c-140">Passar **MAPI_LOGOFF_SHARED** fará com que todos os clientes MAPI iniciem o desligamento e ocorrerá um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="e6c2c-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6c2c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6c2c-141">See also</span></span>



[<span data-ttu-id="e6c2c-142">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6c2c-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="e6c2c-143">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e6c2c-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e6c2c-144">Encerrando uma sessão MAPI</span><span class="sxs-lookup"><span data-stu-id="e6c2c-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

