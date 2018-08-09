---
title: Desenvolvimento de XLLs do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- suplementos - [excel 2007], desenvolvendo XLLs XLLs - [Excel 2007] - [Excel 2007], desenvolvendo
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765272"
---
# <a name="developing-excel-xlls"></a>Desenvolvimento de XLLs do Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O principal motivo para escrever XLLs do Microsoft Excel e usando a API C é criar funções de planilha de alto desempenho. Os aplicativos de funções de alto desempenho — e, iniciando no Excel 2007, a capacidade de gravar interfaces multithreaded aos recursos de servidor poderosas — tornam uma parte muito importante de extensibilidade do Excel. O desempenho dos XLLs ainda mais foi aprimorado no Excel 2007 pela adição de novos tipos de dados e, mais importante, suporte para multithreading.
  
A API C não tem nenhum dos recursos de desenvolvimento rápido de nível superior do Microsoft Visual Basic for Applications (VBA), COM ou o Microsoft .NET Framework. Gerenciamento de memória é baixo nível e, portanto, lança a responsabilidade de maior sobre o desenvolvedor. Muitos recursos do Excel que são expostos por meio de COM, torná-los disponíveis por meio do VBA e o .NET Framework, não estão expostos a API C.


- [Excel Programming Concepts](excel-programming-concepts.md)
  
- [Trabalhar com DLLs](working-with-dlls.md)
  
- [Acessar o código de XLL no Excel](accessing-xll-code-in-excel.md)
  
- [Chamar funções de XLL no Assistente de função ou nas caixas de diálogo Substituir](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Criar XLLs](creating-xlls.md)
  
- [Avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Vários threads e gerenciamento de memória](multithreading-and-memory-management.md)
  
- [Funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md)
  
- [Funções de segurança do cluster](cluster-safe-functions.md)
  
- [Permitir intervenções de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)
  
- [Exibir as caixas de diálogo de dentro de uma DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Acessar a instância do Excel e as alças da janela principal](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Compatibilidade com versões anteriores](backward-compatibility.md)
  

