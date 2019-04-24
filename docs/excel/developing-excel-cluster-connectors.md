---
title: Desenvolver conectores de cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310952"
---
# <a name="developing-excel-cluster-connectors"></a>Desenvolver conectores de cluster do Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Os conectores de cluster do Excel fornecem meios para descarregar automaticamente as chamadas de função definidas pelo usuário com segurança de cluster em um servidor em cluster. Para obter uma descrição das funções definidas pelo usuário com segurança de cluster, consulte [funções de segurança do cluster](cluster-safe-functions.md). Esse descarregamento pode melhorar o desempenho permitindo que mais recursos computacionais sejam usados. Um conector de cluster é normalmente desenvolvido por um fornecedor de cluster de computação de alto desempenho.
  
## <a name="cluster-connectors"></a>Conectores de cluster

Um conector de cluster é uma DLL que fornece pontos de entrada definidos que o Excel usa para coordenar chamadas de função definidas pelo usuário com segurança de cluster. Ele serve como uma interface entre o Excel e o cluster de computação de alto desempenho, para gerenciamento de sessão, para fazer chamadas de função (passando o nome de função totalmente qualificado e os argumentos reais da chamada) e para retornar os resultados da chamada para o Excel por meio de um mecanismo de retorno de chamada.
  
Para criar um conector de cluster, crie uma DLL que expõe os pontos de entrada listados nas [funções do conector de cluster do Excel](excel-cluster-connector-functions.md).
  
## <a name="installing-a-cluster-connector"></a>Instalando um conector de cluster

Para tornar um conector de cluster disponível no Excel, o código de instalação do conector deve instalar a DLL do conector no computador onde o Excel está instalado. Além disso, o código de configuração do conector deve adicionar uma entrada para o conector na seguinte chave do registro:
  
Conectores de cluster do HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel
  
Adicione um nó a essa chave para o conector de cluster que especifica as seguintes cadeias de caracteres:
  
-  `Name`— o nome que aparecerá na lista de conectores de cluster no Excel.
    
-  `Filename`— o caminho completo da DLL.
    

