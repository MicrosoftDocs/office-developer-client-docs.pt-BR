---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410473"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="5b56c-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="5b56c-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="5b56c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b56c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b56c-105">Fornece acesso à tabela de serviço de mensagens, uma lista dos serviços de mensagem no perfil.</span><span class="sxs-lookup"><span data-stu-id="5b56c-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5b56c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b56c-106">Parameters</span></span>

 <span data-ttu-id="5b56c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b56c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5b56c-108">[in] Sempre NULO.</span><span class="sxs-lookup"><span data-stu-id="5b56c-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="5b56c-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5b56c-109">_lppTable_</span></span>
  
> <span data-ttu-id="5b56c-110">[out] Um ponteiro para um ponteiro para a tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5b56c-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b56c-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5b56c-111">Return value</span></span>

<span data-ttu-id="5b56c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b56c-112">S_OK</span></span> 
  
> <span data-ttu-id="5b56c-113">A tabela de serviço de mensagens foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="5b56c-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b56c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b56c-114">Remarks</span></span>

<span data-ttu-id="5b56c-115">O método **IMsgServiceAdmin::GetMsgServiceTable** fornece acesso à tabela de serviço de mensagens, uma tabela que o MAPI mantém que lista os serviços de mensagem atualmente instalados no perfil de sessão.</span><span class="sxs-lookup"><span data-stu-id="5b56c-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="5b56c-116">Para uma lista completa de colunas na tabela de serviço de mensagens, consulte [Message Service Table](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5b56c-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="5b56c-117">A tabela de serviço de mensagens é estática.</span><span class="sxs-lookup"><span data-stu-id="5b56c-117">The message service table is static.</span></span> <span data-ttu-id="5b56c-118">Depois que um cliente recebe acesso a ele, adições ou exclusões subsequentes do serviço de mensagens não o afetará.</span><span class="sxs-lookup"><span data-stu-id="5b56c-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="5b56c-119">Se não houver serviços de mensagem no perfil atual, **GetMsgServiceTable** retornará uma tabela com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="5b56c-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b56c-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5b56c-120">MFCMAPI reference</span></span>

<span data-ttu-id="5b56c-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b56c-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b56c-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5b56c-122">**File**</span></span>|<span data-ttu-id="5b56c-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="5b56c-123">**Function**</span></span>|<span data-ttu-id="5b56c-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="5b56c-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b56c-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5b56c-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="5b56c-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="5b56c-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="5b56c-127">MFCMAPI usa o método **IMsgServiceAdmin::GetMsgServiceTable** para carregar a tabela de serviços em um perfil para renderizar no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="5b56c-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b56c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b56c-128">See also</span></span>



[<span data-ttu-id="5b56c-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="5b56c-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="5b56c-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="5b56c-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="5b56c-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b56c-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="5b56c-132">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5b56c-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

