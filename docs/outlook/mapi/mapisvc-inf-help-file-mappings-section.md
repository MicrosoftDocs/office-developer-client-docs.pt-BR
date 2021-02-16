---
title: Seção MapiSvc.inf [Mapeamentos de Arquivo de Ajuda]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407554"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Seção MapiSvc.inf [Mapeamentos de Arquivo de Ajuda]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **seção [Mapeamentos** de Arquivo de Ajuda] contém entradas que mapeiam um serviço de mensagens para o arquivo que fornece Ajuda para erros gerados pelo serviço. As entradas nesta seção usam o seguinte formato: 
  
 Nome do arquivo de Ajuda do nome do serviço de mensagem **[Mapeamentos** de Arquivo de Ajuda] Nome _do_ arquivo  =   _de Ajuda_
  
O nome do serviço de mensagens é o nome do serviço de mensagens instalado; o nome do arquivo de Ajuda é o nome do arquivo onde residem as informações de erro. O exemplo a seguir mostra uma seção **típica [Mapeamentos** de Arquivo de Ajuda] que contém entradas para três serviços: MAPI, o serviço MsgService e o serviço MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


