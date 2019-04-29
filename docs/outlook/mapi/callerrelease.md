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
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408723"
---
# <a name="callerrelease"></a><span data-ttu-id="a552b-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="a552b-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="a552b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a552b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a552b-105">Define uma função de retorno de chamada que pode liberar um objeto Table Data quando um modo de exibição de tabela está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="a552b-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a552b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a552b-106">Header file:</span></span>  <br/> |<span data-ttu-id="a552b-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="a552b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a552b-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="a552b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a552b-109">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a552b-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="a552b-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="a552b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a552b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a552b-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="a552b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a552b-112">Parameters</span></span>

 <span data-ttu-id="a552b-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="a552b-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="a552b-114">no Dados do chamador salvos por MAPI com o modo de exibição de tabela e passados para a função de retorno de chamada baseada em **CALLERRELEASE** .</span><span class="sxs-lookup"><span data-stu-id="a552b-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="a552b-115">Os dados fornecem contexto sobre a exibição da tabela que está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="a552b-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="a552b-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="a552b-116">_lpTblData_</span></span>
  
> <span data-ttu-id="a552b-117">no Ponteiro para a interface [ITableData: IUnknown](itabledataiunknown.md) do objeto de dados de tabela subjacente à exibição da tabela que está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="a552b-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="a552b-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="a552b-118">_lpVue_</span></span>
  
> <span data-ttu-id="a552b-119">no Ponteiro para a interface imApitable [: IUnknown](imapitableiunknown.md) para o modo de exibição de tabela que está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="a552b-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="a552b-120">Esta é uma interface para o objeto Table retornada no parâmetro _lppMAPITable_ do método [ITableData:: HrGetView](itabledata-hrgetview.md) que criou o objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="a552b-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a552b-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a552b-121">Return value</span></span>

<span data-ttu-id="a552b-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a552b-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a552b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a552b-123">Remarks</span></span>

<span data-ttu-id="a552b-124">Um aplicativo cliente ou provedor de serviços que tenha preenchido um objeto de dados de tabela pode chamar [ITableData:: HrGetView](itabledata-hrgetview.md) para criar um modo de exibição de somente leitura e classificado da tabela.</span><span class="sxs-lookup"><span data-stu-id="a552b-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="a552b-125">A chamada para **HrGetView** passa um ponteiro para uma função de retorno de chamada baseada em **CALLERRELEASE** e também um contexto a ser salvo com o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="a552b-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="a552b-126">Quando a contagem de referência do modo de exibição de tabela retornar a zero e o modo de exibição \*\*\*\* estiver sendo liberado, a implementação imapitada chamará a função de retorno de chamada, passando o contexto no parâmetro _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="a552b-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="a552b-127">Um uso comum de uma função de retorno de chamada baseada em **CALLERRELEASE** é liberar o objeto de dados da tabela subjacente e não ter que controlá-lo durante o processamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="a552b-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

