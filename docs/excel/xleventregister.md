---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303931"
---
# <a name="xleventregister"></a><span data-ttu-id="98bce-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="98bce-103">xlEventRegister</span></span>

 <span data-ttu-id="98bce-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="98bce-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="98bce-105">Usado para registrar um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="98bce-105">Used to register an event handler.</span></span> <span data-ttu-id="98bce-106">Introduzido no Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="98bce-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="98bce-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98bce-107">Parameters</span></span>

 <span data-ttu-id="98bce-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="98bce-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="98bce-109">O nome da função do manipulador de eventos conforme ele aparece no código de DLL.</span><span class="sxs-lookup"><span data-stu-id="98bce-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="98bce-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="98bce-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="98bce-111">O evento manipulado pela função designada no parâmetro _pxProcedure_ .</span><span class="sxs-lookup"><span data-stu-id="98bce-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="98bce-112">A partir do Excel 2010, o Excel oferece suporte aos seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="98bce-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="98bce-113">**Evento**</span><span class="sxs-lookup"><span data-stu-id="98bce-113">**Event**</span></span>|<span data-ttu-id="98bce-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="98bce-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98bce-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="98bce-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="98bce-116">Gerado quando o Excel conclui um cálculo.</span><span class="sxs-lookup"><span data-stu-id="98bce-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="98bce-117">Você pode liberar todos os recursos alocados durante o cálculo após este evento.</span><span class="sxs-lookup"><span data-stu-id="98bce-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="98bce-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="98bce-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="98bce-119">Gerado quando o usuário interrompe o cálculo.</span><span class="sxs-lookup"><span data-stu-id="98bce-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="98bce-120">O XLL deve interromper qualquer atividade assíncrona.</span><span class="sxs-lookup"><span data-stu-id="98bce-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="98bce-121">O evento CalculationEnded é gerado imediatamente após este evento.</span><span class="sxs-lookup"><span data-stu-id="98bce-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="98bce-122">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="98bce-122">Property value/Return value</span></span>

<span data-ttu-id="98bce-123">Se bem-sucedido, retorna **true** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="98bce-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="98bce-124">Se não tiver êxito, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="98bce-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98bce-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="98bce-125">See also</span></span>



[<span data-ttu-id="98bce-126">Funções assíncronas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="98bce-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

