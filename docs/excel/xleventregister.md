---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765467"
---
# <a name="xleventregister"></a><span data-ttu-id="bbccc-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="bbccc-103">xlEventRegister</span></span>

 <span data-ttu-id="bbccc-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bbccc-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bbccc-105">Usado para registrar um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="bbccc-105">Used to register an event handler.</span></span> <span data-ttu-id="bbccc-106">Introduzido no Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="bbccc-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="bbccc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbccc-107">Parameters</span></span>

 <span data-ttu-id="bbccc-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="bbccc-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="bbccc-109">O nome da função handler evento como ele aparece no código DLL.</span><span class="sxs-lookup"><span data-stu-id="bbccc-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="bbccc-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="bbccc-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="bbccc-111">O evento manipulado pela função designada no parâmetro _pxProcedure_ .</span><span class="sxs-lookup"><span data-stu-id="bbccc-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="bbccc-112">Iniciando no Excel 2010, Excel suporta os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="bbccc-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="bbccc-113">**Event**</span><span class="sxs-lookup"><span data-stu-id="bbccc-113">**Event**</span></span>|<span data-ttu-id="bbccc-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bbccc-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bbccc-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="bbccc-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="bbccc-116">Acionado quando um cálculo do Excel completa.</span><span class="sxs-lookup"><span data-stu-id="bbccc-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="bbccc-117">Você pode liberar quaisquer recursos alocados durante o cálculo após este evento.</span><span class="sxs-lookup"><span data-stu-id="bbccc-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="bbccc-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="bbccc-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="bbccc-119">Acionado quando o usuário interrompe o cálculo.</span><span class="sxs-lookup"><span data-stu-id="bbccc-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="bbccc-120">XLL deve parar qualquer atividades assíncronas.</span><span class="sxs-lookup"><span data-stu-id="bbccc-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="bbccc-121">O evento CalculationEnded é disparado imediatamente após este evento.</span><span class="sxs-lookup"><span data-stu-id="bbccc-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="bbccc-122">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bbccc-122">Property value/Return value</span></span>

<span data-ttu-id="bbccc-123">Se tiver êxito, retornará **TRUE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="bbccc-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="bbccc-124">Se for bem sucedida, retornará **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bbccc-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbccc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbccc-125">See also</span></span>



[<span data-ttu-id="bbccc-126">Funções assíncronas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="bbccc-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

