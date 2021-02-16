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
# <a name="handling-events"></a>Manipulando eventos

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A partir do Excel 2010, XLLs podem receber eventos projetados para gerenciar o ciclo de vida da função assíncrona. Os eventos são os seguinte:
  
- **CalculationEnded**: gerado quando o Excel terminar de calcular. Após esse evento, você pode liberar recursos alocados durante o cálculo.
    
- **CalculationCanceled**: gerado quando o usuário interrompe o cálculo. O XLL interrompe qualquer atividade assíncrona. Imediatamente após esse evento, o **evento CalculationEnded** é gerado. 
    
Para manipular esses eventos, o XLL usa a função de API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** e **CalculationCanceled** não são gerados durante o recálculo programático. 
  

