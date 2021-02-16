---
title: Funções seguras de cluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409297"
---
# <a name="cluster-safe-functions"></a>Funções seguras de cluster

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
No Excel 2013, o Excel pode descarregar chamadas User-Defined Function (UDF) para um cluster de computação de alto desempenho por meio de uma interface de conector de cluster dedicada. Os fornecedores de cluster de computação fornecem Conectores de Cluster. Os autores UDF podem declarar suas UDFs como seguras de cluster e, quando um conector de cluster estiver presente, o Excel envia chamadas para essas UDFs para o conector de cluster para descarregamento.
  
Quando o Excel descobre uma UDF segura para cluster durante o recálculo, ele passa o nome do XLL em execução no momento, o nome da UDF segura para cluster e quaisquer parâmetros para o conector do cluster. O conector executa a chamada UDF remotamente e retorna os resultados para o Excel. O cálculo não dependente continua e, quando o conector de cluster termina de executar o UDF, ele passa os resultados para o Excel e os cálculos dependentes continuam. O mecanismo para esse comportamento assíncrono imita o mecanismo usado por UDFs assíncronas, exceto que o conector de cluster gerencia os aspectos assíncronos em vez do autor UDF. Normalmente, um conector de cluster implementa um shim XLL para carregar XLLs e executar UDFs em nós de cluster de computação.
  
A mecânica de declaração de UDFs como seguras para cluster é semelhante às de declarar UDFs como seguras para recálculo multi-threaded. No entanto, como o UDF não está necessariamente sendo executado no mesmo computador que outras UDFs da mesma sessão do Excel, há considerações diferentes ao escrever UDFs seguras para cluster.
  
Para registrar uma UDF como segura para cluster, você deve chamar a função de retorno de chamada [xlfRegister (Formulário 1)](xlfregister-form-1.md) por meio da interface **Excel12** ou **Excel12v.** Para obter mais informações sobre essas interfaces, consulte [Excel4/Excel12](excel4-excel12.md) e [Excel4v/Excel12v](excel4v-excel12v.md). Não há suporte para o registro de uma UDF como segura para cluster por meio da interface **Excel4** ou **Excel4v.** 
  
Se você registrar uma função como segura para cluster, deverá garantir que a função se comporte de maneira segura para cluster. Embora o comportamento exato do conector de cluster seja específico da implementação, você deve projetar o UDF para ser executado em um sistema de computador distribuído e ter as seguintes características:
  
- Uma UDF não deve depender de nenhum estado de memória. Por exemplo, uma UDF não deve depender de um cache existente na memória.
    
- A UDF should not perform Excel callbacks that the cluster connector provider does not support.
    
Além do comportamento seguro para cluster, há as seguintes restrições técnicas em UDFs seguras para cluster:
  
1. Nenhum argumento XLOPER (tipos 'P', 'R').
    
2. Nenhum argumento XLOPER12 que suporte referências de intervalo (tipo 'U').
    
3. Não pode ser uma função equivalente de planilha de macro ('#' e &amp; ' ' não podem ser combinadas).
    
Para UDFs com tempos de execução mais curtos, a sobrecarga de descarregamento pode ser maior do que o tempo que leva para a UDF ser executada, anulando muitos dos benefícios de usar essa infraestrutura.
  
> [!NOTE]
> Você não pode declarar uma UDF segura para cluster como uma UDF assíncrona. 
  
Uma UDF pode determinar se está sendo executado usando um conector de cluster chamando a função de retorno de chamada [xlRunningOnCluster.](xlrunningoncluster.md) 
  

