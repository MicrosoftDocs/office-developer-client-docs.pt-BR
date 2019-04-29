---
title: Funções do conector de cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408583"
---
# <a name="excel-cluster-connector-functions"></a>Funções do conector de cluster do Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
As DLLs do conector de cluster do Microsoft Excel 2013 devem implementar as funções descritas nesta seção.
  
Os valores de retorno mencionados nos tópicos de referência nesta seção são definidos no arquivo de inclusão do SDK, xlcall. h.
  
## <a name="cluster-connector-architecture"></a>Arquitetura do conector de cluster

O Excel chama pontos de entrada em um conector de cluster para transferir chamadas de função definidas pelo usuário para um cluster de computação de alto desempenho e para gerenciamento de sessão de cluster.
  
## <a name="in-this-section"></a>Nesta seção

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Confira também



[Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md)
  
[Funções seguras para clusters](cluster-safe-functions.md)

