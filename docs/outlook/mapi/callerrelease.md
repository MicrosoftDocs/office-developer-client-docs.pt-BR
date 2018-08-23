---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e97e1d5302d8247cb09ce7cb1b581582405300a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568123"
---
# <a name="callerrelease"></a><span data-ttu-id="1c0b2-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="1c0b2-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="1c0b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c0b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c0b2-105">Define uma função de retorno de chamada que pode liberar um objeto de dados de tabela quando um modo de exibição de tabela está sendo lançado.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c0b2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1c0b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c0b2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1c0b2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1c0b2-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="1c0b2-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="1c0b2-109">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="1c0b2-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="1c0b2-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="1c0b2-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="1c0b2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="1c0b2-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="1c0b2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c0b2-112">Parameters</span></span>

 <span data-ttu-id="1c0b2-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="1c0b2-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="1c0b2-114">[in] Dados do chamador salvo pelo MAPI com o modo de exibição de tabela e passado para o **CALLERRELEASE** com base em função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="1c0b2-115">Os dados fornecem contexto sobre o modo de exibição de tabela que está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="1c0b2-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="1c0b2-116">_lpTblData_</span></span>
  
> <span data-ttu-id="1c0b2-117">[in] Ponteiro para o [ITableData: IUnknown](itabledataiunknown.md) interface para o objeto de dados da tabela base na exibição da tabela que está sendo lançada.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="1c0b2-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="1c0b2-118">_lpVue_</span></span>
  
> <span data-ttu-id="1c0b2-119">[in] Ponteiro para o [IMAPITable: IUnknown](imapitableiunknown.md) interface para o modo de exibição de tabela que está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="1c0b2-120">Esta é uma interface para o objeto table retornado no parâmetro _lppMAPITable_ do método [ITableData::HrGetView](itabledata-hrgetview.md) que criou o objeto ao lançamento.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1c0b2-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1c0b2-121">Return value</span></span>

<span data-ttu-id="1c0b2-122">None</span><span class="sxs-lookup"><span data-stu-id="1c0b2-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1c0b2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c0b2-123">Remarks</span></span>

<span data-ttu-id="1c0b2-124">Um aplicativo cliente ou um provedor de serviços que tenha preenchido um objeto de dados de tabela pode chamar [ITableData::HrGetView](itabledata-hrgetview.md) para criar um modo de exibição somente leitura, classificado da tabela.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="1c0b2-125">A chamada para **HrGetView** passa um ponteiro para uma função de retorno de chamada **CALLERRELEASE** com base e também um contexto a ser salvo com o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="1c0b2-126">Quando a contagem de referência do modo de exibição tabela retorna como zero e o modo de exibição está sendo lançado, a implementação de **IMAPITable** chama a função de retorno de chamada, passando o contexto no parâmetro _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="1c0b2-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="1c0b2-127">Um uso comum de uma função de retorno de chamada **CALLERRELEASE** com base é liberar o objeto de dados de tabela base e não precisará ficar atento aos-lo durante o processamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

