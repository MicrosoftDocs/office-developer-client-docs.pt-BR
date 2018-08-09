---
title: Manipular eventos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765369"
---
# <a name="handling-events"></a><span data-ttu-id="fd382-103">Manipular eventos</span><span class="sxs-lookup"><span data-stu-id="fd382-103">Handling Events</span></span>

 <span data-ttu-id="fd382-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fd382-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fd382-105">Iniciando no Excel 2010, XLLs podem receber eventos projetados para gerenciar o ciclo de vida de função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fd382-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="fd382-106">Os eventos são:</span><span class="sxs-lookup"><span data-stu-id="fd382-106">The events are as follows:</span></span>
  
- <span data-ttu-id="fd382-107">**CalculationEnded**: gerado quando o Excel terminar calcular.</span><span class="sxs-lookup"><span data-stu-id="fd382-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="fd382-108">Após este evento, você pode liberar recursos alocados durante o cálculo.</span><span class="sxs-lookup"><span data-stu-id="fd382-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="fd382-109">**CalculationCanceled**: gerado quando o usuário interrompe o cálculo.</span><span class="sxs-lookup"><span data-stu-id="fd382-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="fd382-110">XLL interrompe qualquer atividades assíncronas.</span><span class="sxs-lookup"><span data-stu-id="fd382-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="fd382-111">Imediatamente após este evento, o evento **CalculationEnded** é disparado.</span><span class="sxs-lookup"><span data-stu-id="fd382-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="fd382-112">Para lidar com esses eventos, XLL usa a função do C API [xlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="fd382-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fd382-113">**CalculationEnded** e **CalculationCanceled** não são gerados durante o recálculo programático.</span><span class="sxs-lookup"><span data-stu-id="fd382-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

