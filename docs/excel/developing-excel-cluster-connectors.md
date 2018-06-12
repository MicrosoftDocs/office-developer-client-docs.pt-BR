---
title: Desenvolvendo conectores de Cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765255"
---
# <a name="developing-excel-cluster-connectors"></a>Desenvolvendo conectores de Cluster do Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Conectores de cluster do Excel fornecem um meio de descarregamento automaticamente chamadas de função definida pelo usuário do cluster-safe em um XLL para um servidor em cluster. Para obter uma descrição das funções definidas pelo usuário de cluster-safe, consulte [Funções de segurança do Cluster](cluster-safe-functions.md). Esse descarregamento pode melhorar o desempenho, permitindo que os recursos de computação mais a ser usado. Um conector de cluster geralmente é desenvolvido por um fornecedor de cluster de computação de alto desempenho.
  
## <a name="cluster-connectors"></a>Conectores de cluster

Um conector de cluster é uma DLL que fornece os pontos de entrada definido que o Excel usa para coordenar as chamadas de função definida pelo usuário de cluster-safe. Ela serve como uma interface entre o Excel e o cluster de computação de alto desempenho, para sessão de gerenciamento, para tornar a função chama (passando o nome totalmente qualificado de função e argumentos de reais da chamada) e para retornar resultados de chamada para o Excel por meio de um mecanismo de retorno de chamada.
  
Para criar um conector de cluster, crie uma DLL que expõe os pontos de entrada listados em [Funções de conector de Cluster do Excel](excel-cluster-connector-functions.md).
  
## <a name="installing-a-cluster-connector"></a>Instalando um conector de Cluster

Para disponibilizar um conector de cluster no Excel, o código de programa de instalação do conector deve instalar a DLL do conector no computador onde o Excel está instalado. Além disso, o código de programa de instalação do conector deve adicionar uma entrada para o conector na seguinte chave do registro:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Connectors\ de Cluster
  
Adicione um nó a essa chave para o conector de cluster que especifica as cadeias de caracteres a seguintes:
  
-  `Name`— o nome que aparecerá na lista de conectores de cluster no Excel.
    
-  `Filename`— o caminho completo para a DLL.
    

