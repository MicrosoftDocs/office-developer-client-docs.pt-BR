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
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767726"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="afa4c-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="afa4c-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="afa4c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="afa4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="afa4c-105">Envia uma notificação para uma linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="afa4c-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="afa4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afa4c-106">Parameters</span></span>

 <span data-ttu-id="afa4c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="afa4c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="afa4c-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="afa4c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="afa4c-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="afa4c-109">_cValues_</span></span>
  
> <span data-ttu-id="afa4c-110">[in] A contagem dos valores de propriedade na estrutura [SPropValue](spropvalue.md) apontado pelo parâmetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="afa4c-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="afa4c-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="afa4c-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="afa4c-112">[in] Um ponteiro para uma estrutura **SPropValue** que descreve os valores das colunas na linha destino.</span><span class="sxs-lookup"><span data-stu-id="afa4c-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="afa4c-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="afa4c-113">Return value</span></span>

<span data-ttu-id="afa4c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="afa4c-114">S_OK</span></span> 
  
> <span data-ttu-id="afa4c-115">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="afa4c-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="afa4c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="afa4c-116">Remarks</span></span>

<span data-ttu-id="afa4c-117">O método **ITableData::HrNotify** envia uma notificação de TABLE_ROW_MODIFIED para a linha que corresponde a linha descrita pelas propriedades apontadas pelo parâmetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="afa4c-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="afa4c-118">**HrNotify** envia a notificação independentemente se ocorreram alterações na linha.</span><span class="sxs-lookup"><span data-stu-id="afa4c-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="afa4c-119">Todos os clientes e provedores de serviços que têm modos de exibição da tabela e tem chamado [IMAPITable::Advise](imapitable-advise.md) para registrar para notificações nos seus modos de exibição recebem essa notificação.</span><span class="sxs-lookup"><span data-stu-id="afa4c-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="afa4c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="afa4c-120">See also</span></span>



[<span data-ttu-id="afa4c-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="afa4c-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="afa4c-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="afa4c-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="afa4c-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="afa4c-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

