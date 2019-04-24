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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304035"
---
# <a name="handling-events"></a>Manipulando eventos

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A partir do Excel 2010, os XLLs podem receber eventos projetados para gerenciar o ciclo de vida da função assíncrona. Os eventos são os seguintes:
  
- **CalculationEnded**: ocorre quando o Excel conclui o cálculo. Após esse evento, você pode liberar recursos alocados durante o cálculo.
    
- **CalculationCanceled**: ocorre quando o usuário interrompe o cálculo. O XLL interrompe qualquer atividade assíncrona. Imediatamente após este evento, o evento **CalculationEnded** é gerado. 
    
Para lidar com esses eventos, o XLL usa a função da API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** e **CalculationCanceled** não são gerados durante o recálculo programático. 
  

