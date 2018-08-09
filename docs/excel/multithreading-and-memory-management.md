---
title: Vários threads e gerenciamento de memória
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765423"
---
# <a name="multithreading-and-memory-management"></a>Vários threads e gerenciamento de memória

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Manipulação adequada de memória é vital para a criação de suplementos XLL confiáveis para o Microsoft Excel. Falha ao alocar buffers de memória apropriado e liberá-los quando eles não são mais necessários reduz o desempenho, cria contenção de recursos e destabilizes Excel.
  
A partir do Microsoft Office Excel 2007, você pode configurar o Excel para usar até 1.024 segmentos simultâneos durante o recálculo. Em alguns casos, especialmente quando vários processadores estão disponíveis ou com definidas pelo usuário funções em execução em servidores clusterizados multithreading podem melhorar o desempenho.
  
Os tópicos a seguir descrevem como gerenciar memória e threads em XLLs:
  
- [Gerenciamento de memória no Excel](memory-management-in-excel.md)
    
- [Vários threads e contenção da memória no Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Recálculo do vários threads no Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Confira também



[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

