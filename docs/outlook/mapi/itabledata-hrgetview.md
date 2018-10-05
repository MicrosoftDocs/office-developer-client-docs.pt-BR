---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398707"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="0c7d0-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="0c7d0-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="0c7d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c7d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c7d0-105">Cria um modo de exibição de tabela, retornando um ponteiro para uma implementação [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="0c7d0-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="0c7d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c7d0-106">Parameters</span></span>

 <span data-ttu-id="0c7d0-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="0c7d0-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="0c7d0-108">[in] Um ponteiro para uma estrutura de ordem de classificação que descreve a ordem de classificação para o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="0c7d0-109">Se o parâmetro _lpSSortOrderSet_ é passado NULL, o modo de exibição não será classificado.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="0c7d0-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="0c7d0-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="0c7d0-111">[in] Um ponteiro para uma função de retorno de chamada com base em protótipo [CALLERRELEASE](callerrelease.md) que chamadas MAPI quando ele libera o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="0c7d0-112">Se NULL é passada no parâmetro _lpfCallerRelease_ , nenhuma função é chamada na versão do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="0c7d0-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="0c7d0-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="0c7d0-114">[in] Os dados que devem ser passados para a função de retorno de chamada apontada pela _lpfCallerRelease_e salvo com o novo modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="0c7d0-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="0c7d0-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="0c7d0-116">[out] Um ponteiro para um ponteiro para o modo de exibição recém-criado.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c7d0-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0c7d0-117">Return value</span></span>

<span data-ttu-id="0c7d0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c7d0-118">S_OK</span></span> 
  
> <span data-ttu-id="0c7d0-119">O modo de exibição foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c7d0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c7d0-120">Remarks</span></span>

<span data-ttu-id="0c7d0-121">O método **ITableData::HrGetView** cria uma exibição somente leitura dos dados na tabela, classificada na ordem apontada pelo parâmetro _lpSSortOrderSet_ .</span><span class="sxs-lookup"><span data-stu-id="0c7d0-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="0c7d0-122">O cursor é colocado no início da primeira linha no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="0c7d0-123">Uma implementação de interface **IMAPITable** para acessar o modo de exibição será retornada.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="0c7d0-124">Provedores de serviços de chamarem **HrGetView** sempre que precisarem dar um acesso para cliente a uma tabela.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="0c7d0-125">**HrGetView** cria o modo de exibição e retorna o ponteiro **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="0c7d0-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="0c7d0-126">Provedores de serviços por sua vez passam o ponteiro para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="0c7d0-127">Quando o cliente for concluído, usando a tabela e chama o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** chama a função de retorno de chamada apontada pelo parâmetro _lpfCallerRelease_ .</span><span class="sxs-lookup"><span data-stu-id="0c7d0-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="0c7d0-128">Se precisa de um provedor de serviços retornar a um cliente de um modo de exibição que tenha uma coluna personalizada definida ou uma restrição, o provedor pode chamar métodos do modo de exibição de [IMAPITable::SetColumns](imapitable-setcolumns.md) e [IMAPITable:: Restrict](imapitable-restrict.md) antes de permitir o acesso do cliente.</span><span class="sxs-lookup"><span data-stu-id="0c7d0-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c7d0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c7d0-129">See also</span></span>



[<span data-ttu-id="0c7d0-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="0c7d0-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="0c7d0-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c7d0-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="0c7d0-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="0c7d0-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="0c7d0-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c7d0-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

