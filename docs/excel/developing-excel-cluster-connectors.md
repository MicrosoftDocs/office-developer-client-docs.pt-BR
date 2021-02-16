---
title: Desenvolvendo conectores de cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412594"
---
# <a name="developing-excel-cluster-connectors"></a>Desenvolvendo conectores de cluster do Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Os conectores de cluster do Excel fornecem um meio para descarregamento automático de chamadas de função definida pelo usuário seguras para cluster em um XLL para um servidor em cluster. Para uma descrição de funções definidas pelo usuário seguras para cluster, consulte [Funções seguras de cluster.](cluster-safe-functions.md) Esse descarregamento pode melhorar o desempenho, permitindo que mais recursos de computação sejam usados. Um conector de cluster geralmente é desenvolvido por um fornecedor de cluster de computação de alto desempenho.
  
## <a name="cluster-connectors"></a>Conectores de cluster

Um conector de cluster é uma DLL que fornece pontos de entrada definidos que o Excel usa para coordenar chamadas de função definidas pelo usuário seguras para cluster. Ele serve como uma interface entre o Excel e o cluster de computação de alto desempenho, para gerenciamento de sessão, para fazer chamadas de função (passando o nome da função totalmente qualificada e os argumentos reais da chamada) e para retornar resultados de chamada para o Excel por meio de um mecanismo de retorno de chamada.
  
Para criar um conector de cluster, crie uma DLL que exponha os pontos de entrada listados em Funções do [Conector de Cluster do Excel.](excel-cluster-connector-functions.md)
  
## <a name="installing-a-cluster-connector"></a>Instalando um conector de cluster

Para disponibilizar um conector de cluster no Excel, o código de instalação do conector deve instalar a DLL do conector no computador em que o Excel está instalado. Além disso, o código de instalação do conector deve adicionar uma entrada para o conector sob a seguinte chave do Registro:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Adicione um nó a essa chave para o conector de cluster que especifica as seguintes cadeias de caracteres:
  
-  `Name`—o nome que aparecerá na lista de conectores de cluster no Excel.
    
-  `Filename`— o caminho completo para a DLL.
    

