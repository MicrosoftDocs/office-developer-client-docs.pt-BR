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
  
No Excel 2013, o Excel pode descarregar chamadas de função definida pelo usuário (UDF) para um cluster de computação de alto desempenho por meio de uma interface de conector de cluster dedicado. Os fornecedores de cluster de computação fornecem conectores de cluster. Os autores de UDF podem declarar seus UDFs como seguros de cluster e, quando um conector de cluster estiver presente, o Excel enviará chamadas para esses UDFs para o conector de cluster para descarregamento.
  
Quando o Excel descobre um UDF seguro de cluster durante o recálculo, ele passa o nome do XLL atualmente em execução, o nome do UDF com segurança de cluster e todos os parâmetros para o conector de cluster. O conector executa a chamada UDF remotamente e retorna os resultados para o Excel. O cálculo não dependente continua e quando o conector do cluster termina de executar o UDF, ele passa os resultados para o Excel e os cálculos dependentes continuam. O mecanismo para esse comportamento assíncrono imita o mecanismo usado por UDFs assíncronas, exceto pelo fato de o conector de cluster gerenciar os aspectos assíncronos em vez do autor do UDF. Normalmente, um conector de cluster implementa uma Shim de XLL para carregar XLLs e executar UDFs em nós de cluster de computadores.
  
A mecânica da declaração de UDFs como em cluster é semelhante àquelas da declaração de UDFs como seguros para o recálculo de vários threads. No enTanto, como o UDF não está necessariamente em execução no mesmo computador que outros UDFs da mesma sessão do Excel, há diferentes considerações ao gravar UDFs com segurança de cluster.
  
Para registrar um UDF como protegido por cluster, você deve chamar a função de retorno de chamada [xlfRegister (formulário 1)](xlfregister-form-1.md) através da interface **Excel12** ou **Excel12v** . Para obter mais informações sobre essas interfaces, consulte o [Excel4/Excel12](excel4-excel12.md) e o [Excel4v/Excel12v](excel4v-excel12v.md). Não há suporte para o registro de um UDF como protegido por cluster por meio da interface **Excel4** ou **Excel4v** . 
  
Se você registrar uma função como segura para cluster, deverá garantir que a função se comformará em um modo de segurança do cluster. Embora o comportamento exato do conector de cluster seja específico da implementação, você deve projetar seu UDF para ser executado em um sistema de computador distribuído e ter as seguintes características:
  
- Um UDF não deve depender de nenhum estado de memória. Por exemplo, um UDF não deve confiar em um cache existente na memória.
    
- Um UDF não deve executar retornos de chamada do Excel para os quais o provedor do conector de cluster não ofereça suporte.
    
Além do comportamento de cluster seguro, existem as seguintes restrições técnicas em UDFs com segurança de cluster:
  
1. Nenhum argumento XLOPER (tipos ' P ', ' R ').
    
2. Nenhum argumento XLOPER12 que oferece suporte a referências de intervalo (tipo ' U ').
    
3. Não pode ser uma função equivalente de planilha de macro (' #&amp;' e ' ' não podem ser combinados).
    
Para UDFs com tempos de execução mais curtos, a sobrecarga de descarregamento pode ser maior do que o tempo que o UDF leva para ser executado, eliminando muitos dos benefícios de usar essa infraestrutura.
  
> [!NOTE]
> Você não pode declarar um UDF com segurança de cluster como um UDF assíncrono. 
  
Um UDF pode determinar se ele está sendo executado usando um conector de cluster chamando a função de retorno de chamada [xlRunningOnCluster](xlrunningoncluster.md) . 
  

