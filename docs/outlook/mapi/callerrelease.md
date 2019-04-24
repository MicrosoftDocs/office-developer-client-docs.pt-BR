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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331840"
---
# <a name="callerrelease"></a><span data-ttu-id="f080f-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="f080f-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="f080f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f080f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f080f-105">Define uma função de retorno de chamada que pode liberar um objeto Table Data quando um modo de exibição de tabela está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="f080f-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f080f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f080f-106">Header file:</span></span>  <br/> |<span data-ttu-id="f080f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f080f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f080f-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="f080f-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="f080f-109">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="f080f-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="f080f-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="f080f-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="f080f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="f080f-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="f080f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f080f-112">Parameters</span></span>

 <span data-ttu-id="f080f-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="f080f-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="f080f-114">no Dados do chamador salvos por MAPI com o modo de exibição de tabela e passados para a função de retorno de chamada baseada em **CALLERRELEASE** .</span><span class="sxs-lookup"><span data-stu-id="f080f-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="f080f-115">Os dados fornecem contexto sobre a exibição da tabela que está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="f080f-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="f080f-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="f080f-116">_lpTblData_</span></span>
  
> <span data-ttu-id="f080f-117">no Ponteiro para a interface [ITableData: IUnknown](itabledataiunknown.md) do objeto de dados de tabela subjacente à exibição da tabela que está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="f080f-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="f080f-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="f080f-118">_lpVue_</span></span>
  
> <span data-ttu-id="f080f-119">no Ponteiro para a interface imApitable [: IUnknown](imapitableiunknown.md) para o modo de exibição de tabela que está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="f080f-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="f080f-120">Esta é uma interface para o objeto Table retornada no parâmetro _lppMAPITable_ do método [ITableData:: HrGetView](itabledata-hrgetview.md) que criou o objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="f080f-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f080f-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f080f-121">Return value</span></span>

<span data-ttu-id="f080f-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f080f-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f080f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f080f-123">Remarks</span></span>

<span data-ttu-id="f080f-124">Um aplicativo cliente ou provedor de serviços que tenha preenchido um objeto de dados de tabela pode chamar [ITableData:: HrGetView](itabledata-hrgetview.md) para criar um modo de exibição de somente leitura e classificado da tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="f080f-125">A chamada para **HrGetView** passa um ponteiro para uma função de retorno de chamada baseada em **CALLERRELEASE** e também um contexto a ser salvo com o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="f080f-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="f080f-126">Quando a contagem de referência do modo de exibição de tabela retornar a zero e o modo de exibição \*\*\*\* estiver sendo liberado, a implementação imapitada chamará a função de retorno de chamada, passando o contexto no parâmetro _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="f080f-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="f080f-127">Um uso comum de uma função de retorno de chamada baseada em **CALLERRELEASE** é liberar o objeto de dados da tabela subjacente e não ter que controlá-lo durante o processamento subsequente.</span><span class="sxs-lookup"><span data-stu-id="f080f-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

