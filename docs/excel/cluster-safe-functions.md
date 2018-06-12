---
title: Funções de segurança de cluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765252"
---
# <a name="cluster-safe-functions"></a>Funções de segurança de cluster

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
No Excel 2013, Excel pode descarregamento de chamadas de função definida pelo usuário (UDF) para um cluster de computação de alto desempenho por meio de uma interface de conector de cluster dedicado. Compute cluster fornecedores fornecem conectores de Cluster. Os autores do UDF podem declarar seus UDFs como cluster seguros e, quando um conector de cluster estiver presente, o Excel envia chamadas para esses UDFs para o conector de cluster para descarregamento.
  
Quando o Excel descobre um UDF seguras do cluster durante o recálculo, ele passa o nome da XLL que está sendo executado, o nome do UDF seguras do cluster e qualquer parâmetro para o conector de cluster. O conector é executado a chamada UDF remotamente e retorna os resultados para o Excel. Cálculo dependentes não continuará e quando o conector de cluster concluiu a execução do UDF, ele passa os resultados para o Excel e continuam cálculos dependentes. O mecanismo para esse comportamento assíncrono simule o mecanismo usado pela UDFs assíncronas, exceto pelo fato do conector de cluster gerencia os aspectos assíncronos, em vez de autor UDF. Normalmente, um conector de cluster implementa uma correção XLL para carregar XLLs e execute UDFs em compute nós do cluster.
  
A mecânica da declarando UDFs como cluster-safe são semelhantes às declarando UDFs como seguros para recálculo multithread. No entanto, porque o UDF não necessariamente estiver em execução no mesmo computador que outros UDFs da mesma sessão do Excel, existem diferentes considerações ao escrever UDFs seguras do cluster.
  
Para registrar um UDF como seguras do cluster, você deve chamar a função de retorno de chamada [xlfRegister (formulário 1)](xlfregister-form-1.md) por meio da interface **Excel12** ou **Excel12v** . Para obter mais informações sobre essas interfaces, consulte o [Excel4/Excel12](excel4-excel12.md) e [Excel4v/Excel12v](excel4v-excel12v.md). Registrando um UDF como não há suporte para cluster-safe por meio da interface do **Excel4** ou **Excel4v** . 
  
Se você registrar uma função como cluster-safe, certifique-se de que a função se comporta de forma segura de cluster. Embora o comportamento exato do conector do cluster é específico da implementação, você deve projetar sua UDF sejam executados em um sistema de computador distribuído e que têm as seguintes características:
  
- Um UDF não deve confiar em qualquer estado de memória. Por exemplo, um UDF não deve confiar em um cache de memória existente.
    
- Um UDF não deve realizar retornos de chamada do Excel que não suporta o provedor do conector de cluster.
    
Além de comportamento de cluster-safe, existem as seguintes restrições técnicas sobre UDFs seguras do cluster:
  
1. Sem argumentos XLOPER (tipos 'P', 'R').
    
2. Sem argumentos XLOPER12 que oferecem suporte a referências de intervalo (tipo 'U').
    
3. Não pode ser uma função equivalente de folha de macro ('#' e '&amp;' não pode ser combinado).
    
Para UDFs com mais curto tempo de execução, a sobrecarga de descarregamento pode ser maior do que o tempo que leva UDF ser executados, eliminando muitos dos benefícios do uso dessa infra-estrutura.
  
> [!NOTE]
> Você não pode declarar um UDF seguras do cluster como uma UDF assíncrona. 
  
Um UDF para determinar se ele está sendo executado usando um conector de cluster chamando a função de retorno de chamada [xlRunningOnCluster](xlrunningoncluster.md) . 
  

