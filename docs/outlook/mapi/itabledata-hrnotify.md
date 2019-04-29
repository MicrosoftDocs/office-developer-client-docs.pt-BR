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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413266"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="05f5d-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="05f5d-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="05f5d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05f5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05f5d-105">Envia uma notificação para uma linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="05f5d-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="05f5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05f5d-106">Parameters</span></span>

 <span data-ttu-id="05f5d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05f5d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="05f5d-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="05f5d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="05f5d-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="05f5d-109">_cValues_</span></span>
  
> <span data-ttu-id="05f5d-110">no A contagem de valores de propriedade na estrutura [SPropValue](spropvalue.md) apontada pelo parâmetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="05f5d-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="05f5d-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="05f5d-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="05f5d-112">no Um ponteiro para uma estrutura **SPropValue** que descreve os valores das colunas na linha de destino.</span><span class="sxs-lookup"><span data-stu-id="05f5d-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="05f5d-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="05f5d-113">Return value</span></span>

<span data-ttu-id="05f5d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="05f5d-114">S_OK</span></span> 
  
> <span data-ttu-id="05f5d-115">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="05f5d-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05f5d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="05f5d-116">Remarks</span></span>

<span data-ttu-id="05f5d-117">O método **ITableData:: HrNotify** envia uma notificação TABLE_ROW_MODIFIED para a linha que corresponde à linha descrita pelas propriedades apontadas pelo parâmetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="05f5d-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="05f5d-118">O **HrNotify** envia a notificação independentemente de ocorrerem alterações na linha.</span><span class="sxs-lookup"><span data-stu-id="05f5d-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="05f5d-119">Todos os clientes e provedores de serviço que possuem modos de exibição da tabela e chamaram imApitable [:: Advise](imapitable-advise.md) para registrar notificações em seus modos de exibição recebem esta notificação.</span><span class="sxs-lookup"><span data-stu-id="05f5d-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="05f5d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="05f5d-120">See also</span></span>



[<span data-ttu-id="05f5d-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="05f5d-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="05f5d-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="05f5d-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="05f5d-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05f5d-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

