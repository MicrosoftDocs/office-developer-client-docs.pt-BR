---
title: Manipulando eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438264"
---
# <a name="handling-events"></a><span data-ttu-id="5f5a1-103">Manipulando eventos</span><span class="sxs-lookup"><span data-stu-id="5f5a1-103">Handling Events</span></span>

 <span data-ttu-id="5f5a1-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5f5a1-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5f5a1-105">A partir do Excel 2010, XLLs podem receber eventos projetados para gerenciar o ciclo de vida da função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5f5a1-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="5f5a1-106">Os eventos são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="5f5a1-106">The events are as follows:</span></span>
  
- <span data-ttu-id="5f5a1-107">**CalculationEnded**: gerado quando o Excel terminar de calcular.</span><span class="sxs-lookup"><span data-stu-id="5f5a1-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="5f5a1-108">Após esse evento, você pode liberar recursos alocados durante o cálculo.</span><span class="sxs-lookup"><span data-stu-id="5f5a1-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="5f5a1-109">**CalculationCanceled**: gerado quando o usuário interrompe o cálculo.</span><span class="sxs-lookup"><span data-stu-id="5f5a1-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="5f5a1-110">O XLL interrompe qualquer atividade assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5f5a1-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="5f5a1-111">Imediatamente após esse evento, o **evento CalculationEnded** é gerado.</span><span class="sxs-lookup"><span data-stu-id="5f5a1-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="5f5a1-112">Para manipular esses eventos, o XLL usa a função de API C [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="5f5a1-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5f5a1-113">**CalculationEnded** e **CalculationCanceled** não são gerados durante o recálculo programático.</span><span class="sxs-lookup"><span data-stu-id="5f5a1-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

