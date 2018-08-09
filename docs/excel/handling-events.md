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
# <a name="handling-events"></a>Manipular eventos

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Iniciando no Excel 2010, XLLs podem receber eventos projetados para gerenciar o ciclo de vida de função assíncrona. Os eventos são:
  
- **CalculationEnded**: gerado quando o Excel terminar calcular. Após este evento, você pode liberar recursos alocados durante o cálculo.
    
- **CalculationCanceled**: gerado quando o usuário interrompe o cálculo. XLL interrompe qualquer atividades assíncronas. Imediatamente após este evento, o evento **CalculationEnded** é disparado. 
    
Para lidar com esses eventos, XLL usa a função do C API [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** e **CalculationCanceled** não são gerados durante o recálculo programático. 
  

