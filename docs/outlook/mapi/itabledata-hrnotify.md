---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 20831901567f177ada70a6cea94db0537786db94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571434"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="66ba2-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="66ba2-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="66ba2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66ba2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66ba2-105">Envia uma notificação para uma linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="66ba2-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="66ba2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66ba2-106">Parameters</span></span>

 <span data-ttu-id="66ba2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="66ba2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="66ba2-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="66ba2-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="66ba2-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="66ba2-109">_cValues_</span></span>
  
> <span data-ttu-id="66ba2-110">[in] A contagem dos valores de propriedade na estrutura [SPropValue](spropvalue.md) apontado pelo parâmetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="66ba2-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="66ba2-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="66ba2-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="66ba2-112">[in] Um ponteiro para uma estrutura **SPropValue** que descreve os valores das colunas na linha destino.</span><span class="sxs-lookup"><span data-stu-id="66ba2-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="66ba2-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="66ba2-113">Return value</span></span>

<span data-ttu-id="66ba2-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="66ba2-114">S_OK</span></span> 
  
> <span data-ttu-id="66ba2-115">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="66ba2-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66ba2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="66ba2-116">Remarks</span></span>

<span data-ttu-id="66ba2-117">O método **ITableData::HrNotify** envia uma notificação de TABLE_ROW_MODIFIED para a linha que corresponde a linha descrita pelas propriedades apontadas pelo parâmetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="66ba2-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="66ba2-118">**HrNotify** envia a notificação independentemente se ocorreram alterações na linha.</span><span class="sxs-lookup"><span data-stu-id="66ba2-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="66ba2-119">Todos os clientes e provedores de serviços que têm modos de exibição da tabela e tem chamado [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações nos seus modos de exibição recebem essa notificação.</span><span class="sxs-lookup"><span data-stu-id="66ba2-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66ba2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="66ba2-120">See also</span></span>



[<span data-ttu-id="66ba2-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="66ba2-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="66ba2-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="66ba2-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="66ba2-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66ba2-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

