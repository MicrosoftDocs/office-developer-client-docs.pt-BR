---
title: Gerenciamento de memória e multithreading
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414463"
---
# <a name="multithreading-and-memory-management"></a>Gerenciamento de memória e multithreading

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A manipulação adequada da memória é vital para a criação de suplementos XLL confiáveis para o Microsoft Excel. Falha ao alocar buffers de memória apropriados e liberá-los quando eles não são mais necessários reduzem o desempenho, criam contenção de recursos e desestabilizam o Excel.
  
A partir do Microsoft Office Excel 2007, você pode configurar o Excel para usar até 1.024 threads simultâneos ao recalcular. Em alguns casos, especialmente quando vários processadores estão disponíveis ou com funções definidas pelo usuário em execução em servidores em cluster, o multithreading pode melhorar o desempenho.
  
Os tópicos a seguir descrevem como gerenciar memória e threads em XLLs:
  
- [Gerenciamento de Memória no Excel](memory-management-in-excel.md)
    
- [Multithreading e conTenção de memória no Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Confira também



[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

