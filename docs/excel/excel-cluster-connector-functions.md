---
title: Funções de conector de Cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765292"
---
# <a name="excel-cluster-connector-functions"></a>Funções de conector de Cluster do Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Conector de cluster do Microsoft Excel 2013 DLLs deve implementar as funções descritas nesta seção.
  
Os valores de retorno mencionados na referência tópicos desta seção são definidos no SDK incluam o arquivo, xlcall. h.
  
## <a name="cluster-connector-architecture"></a>Arquitetura de conector de cluster

Excel chama os pontos de entrada em um conector de cluster para transferir chamadas de função definida pelo usuário para um cluster de computação de alto desempenho e para o gerenciamento de sessão do cluster.
  
## <a name="in-this-section"></a>Nesta se��o

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Confira também



[Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md)
  
[Funções de segurança de cluster](cluster-safe-functions.md)

