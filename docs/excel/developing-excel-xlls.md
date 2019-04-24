---
title: Desenvolvimento de XLLs do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- suplementos, [excel 2007,] desenvolvendo XLLs - [Excel 2007] - [Excel 2007] desenvolver
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301656"
---
# <a name="developing-excel-xlls"></a>Desenvolvimento de XLLs do Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A principal razão para gravar Microsoft Excel XLLs e usar a API de C é criar funções de planilha de alto desempenho. No entanto, os aplicativos de funções de alto desempenho, e no Excel 2007, a capacidade de gravar interfaces de vários threads em recursos avançados do servidor, fazem disso uma parte muito importante da extensibilidade do Excel. O desempenho XLLs mais avançado no Excel 2007, a adição de novos tipos de dados e mais importante, suporte para multithread.
  
A API de C não tem nenhum dos recursos de desenvolvimento rápido do Microsoft Visual Basic para aplicativos (VBA), COM ou Microsoft .NET Framework. O gerenciamento de memória é de nível baixo e, portanto, atribui uma maior responsabilidade ao desenvolvedor. Muitos recursos do Excel que são expostos pelo COM, tornando-os disponíveis por meio do VBA e o .NET Framework, não são expostos à API de C.


- [Conceitos de programação do Excel](excel-programming-concepts.md)
  
- [Trabalhar com DLLs](working-with-dlls.md)
  
- [Acessar o código de XLL no Excel](accessing-xll-code-in-excel.md)
  
- [Chamar funções de XLL no Assistente de Função ou Substituir nas caixas de diálogo](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Chamada para o Excel da DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Como criar XLLs](creating-xlls.md)
  
- [Avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Gerenciamento de memória e multithreading](multithreading-and-memory-management.md)
  
- [Funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md)
  
- [Funções seguras para clusters](cluster-safe-functions.md)
  
- [Permitir intervenções de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)
  
- [Exibir caixas de diálogo de dentro de uma DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Compatibilidade com versões anteriores](backward-compatibility.md)
  

