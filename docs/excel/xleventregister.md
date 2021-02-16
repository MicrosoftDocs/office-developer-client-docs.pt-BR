---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160276"
---
# <a name="xleventregister"></a><span data-ttu-id="5673c-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="5673c-103">xlEventRegister</span></span>

 <span data-ttu-id="5673c-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5673c-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5673c-105">Usado para registrar um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5673c-105">Used to register an event handler.</span></span> <span data-ttu-id="5673c-106">Introduzido no Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="5673c-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="5673c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5673c-107">Parameters</span></span>

 <span data-ttu-id="5673c-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="5673c-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="5673c-109">O nome da função do manipulador de eventos como aparece no código DLL.</span><span class="sxs-lookup"><span data-stu-id="5673c-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="5673c-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="5673c-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="5673c-111">O evento manipulado pela função designada no _parâmetro pxProcedure._</span><span class="sxs-lookup"><span data-stu-id="5673c-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="5673c-112">A partir do Excel 2010, o Excel dá suporte aos seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="5673c-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="5673c-113">**Evento**</span><span class="sxs-lookup"><span data-stu-id="5673c-113">**Event**</span></span>|<span data-ttu-id="5673c-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5673c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5673c-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="5673c-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="5673c-116">Gerado quando o Excel conclui um cálculo.</span><span class="sxs-lookup"><span data-stu-id="5673c-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="5673c-117">Você pode liberar todos os recursos alocados durante o cálculo após esse evento.</span><span class="sxs-lookup"><span data-stu-id="5673c-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="5673c-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="5673c-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="5673c-119">Gerado quando o usuário interrompe o cálculo.</span><span class="sxs-lookup"><span data-stu-id="5673c-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="5673c-120">O XLL deve parar qualquer atividade assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5673c-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="5673c-121">O evento CalculationEnded é gerado imediatamente após esse evento.</span><span class="sxs-lookup"><span data-stu-id="5673c-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="5673c-122">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5673c-122">Property value/Return value</span></span>

<span data-ttu-id="5673c-123">Se bem-sucedido, pxRes (**xltypeInt**) tem um valor > 0.</span><span class="sxs-lookup"><span data-stu-id="5673c-123">If successful, pxRes (**xltypeInt**) has a value > 0.</span></span> <span data-ttu-id="5673c-124">Se não tiver êxito, pxRes ==0.</span><span class="sxs-lookup"><span data-stu-id="5673c-124">If unsuccessful, pxRes ==0.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5673c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5673c-125">See also</span></span>



[<span data-ttu-id="5673c-126">Funções assíncronas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5673c-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

