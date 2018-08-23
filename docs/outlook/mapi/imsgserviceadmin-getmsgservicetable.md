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
ms.openlocfilehash: 5d8e91490cc39c3f259d35a923bb3bcbb2bf6011
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568165"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="13e3a-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="13e3a-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="13e3a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13e3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13e3a-105">Fornece acesso à tabela de serviço de mensagem, uma lista dos serviços de mensagem no perfil.</span><span class="sxs-lookup"><span data-stu-id="13e3a-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="13e3a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e3a-106">Parameters</span></span>

 <span data-ttu-id="13e3a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13e3a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="13e3a-108">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="13e3a-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="13e3a-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="13e3a-109">_lppTable_</span></span>
  
> <span data-ttu-id="13e3a-110">[out] Um ponteiro para um ponteiro para a tabela de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="13e3a-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13e3a-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="13e3a-111">Return value</span></span>

<span data-ttu-id="13e3a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e3a-112">S_OK</span></span> 
  
> <span data-ttu-id="13e3a-113">A tabela de serviços de mensagem foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="13e3a-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13e3a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="13e3a-114">Remarks</span></span>

<span data-ttu-id="13e3a-115">O método **IMsgServiceAdmin::GetMsgServiceTable** fornece acesso à tabela de serviço de mensagem, uma tabela que mantém MAPI que lista os serviços de mensagem instalados atualmente no perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="13e3a-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="13e3a-116">Para obter uma lista completa das colunas na tabela de serviço de mensagens, consulte a [Tabela de serviços de mensagem](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="13e3a-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="13e3a-117">A tabela de serviços de mensagem é estática.</span><span class="sxs-lookup"><span data-stu-id="13e3a-117">The message service table is static.</span></span> <span data-ttu-id="13e3a-118">Depois que um cliente tem acesso a ele, adições de serviço de mensagem subsequente ou exclusões não afetará-lo.</span><span class="sxs-lookup"><span data-stu-id="13e3a-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="13e3a-119">Se não houver nenhuma mensagem serviços no perfil atual, **GetMsgServiceTable** retorna uma tabela com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="13e3a-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="13e3a-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="13e3a-120">MFCMAPI reference</span></span>

<span data-ttu-id="13e3a-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="13e3a-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="13e3a-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="13e3a-122">**File**</span></span>|<span data-ttu-id="13e3a-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="13e3a-123">**Function**</span></span>|<span data-ttu-id="13e3a-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="13e3a-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13e3a-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="13e3a-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="13e3a-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="13e3a-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="13e3a-127">MFCMAPI usa o método **IMsgServiceAdmin::GetMsgServiceTable** para carregar a tabela de serviços em um perfil para renderizar no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="13e3a-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13e3a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="13e3a-128">See also</span></span>



[<span data-ttu-id="13e3a-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="13e3a-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="13e3a-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="13e3a-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="13e3a-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13e3a-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="13e3a-132">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="13e3a-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

