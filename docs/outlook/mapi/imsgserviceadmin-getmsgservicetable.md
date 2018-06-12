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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 588a32cb2a468c84dfc513af5e4abf6a9a1d0286
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767516"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="0d0b7-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="0d0b7-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="0d0b7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d0b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d0b7-105">Fornece acesso à tabela de serviço de mensagem, uma lista dos serviços de mensagem no perfil.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="0d0b7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0d0b7-106">Parameters</span></span>

 <span data-ttu-id="0d0b7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d0b7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0d0b7-108">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="0d0b7-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="0d0b7-109">_lppTable_</span></span>
  
> <span data-ttu-id="0d0b7-110">[out] Um ponteiro para um ponteiro para a tabela de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d0b7-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0d0b7-111">Return value</span></span>

<span data-ttu-id="0d0b7-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d0b7-112">S_OK</span></span> 
  
> <span data-ttu-id="0d0b7-113">A tabela de serviços de mensagem foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d0b7-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0d0b7-114">Remarks</span></span>

<span data-ttu-id="0d0b7-115">O método **IMsgServiceAdmin::GetMsgServiceTable** fornece acesso à tabela de serviço de mensagem, uma tabela que mantém MAPI que lista os serviços de mensagem instalados atualmente no perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="0d0b7-116">Para obter uma lista completa das colunas na tabela de serviço de mensagens, consulte a [Tabela de serviços de mensagem](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0d0b7-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="0d0b7-117">A tabela de serviços de mensagem é estática.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-117">The message service table is static.</span></span> <span data-ttu-id="0d0b7-118">Depois que um cliente tem acesso a ele, adições de serviço de mensagem subsequente ou exclusões não afetará-lo.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="0d0b7-119">Se não houver nenhuma mensagem serviços no perfil atual, **GetMsgServiceTable** retorna uma tabela com zero linhas.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0d0b7-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0d0b7-120">MFCMAPI reference</span></span>

<span data-ttu-id="0d0b7-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0d0b7-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0d0b7-122">**File**</span></span>|<span data-ttu-id="0d0b7-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="0d0b7-123">**Function**</span></span>|<span data-ttu-id="0d0b7-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0d0b7-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d0b7-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0d0b7-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="0d0b7-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="0d0b7-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="0d0b7-127">MFCMAPI usa o método **IMsgServiceAdmin::GetMsgServiceTable** para carregar a tabela de serviços em um perfil para renderizar no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d0b7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d0b7-128">See also</span></span>



[<span data-ttu-id="0d0b7-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="0d0b7-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="0d0b7-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="0d0b7-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="0d0b7-131">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d0b7-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="0d0b7-132">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0d0b7-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

