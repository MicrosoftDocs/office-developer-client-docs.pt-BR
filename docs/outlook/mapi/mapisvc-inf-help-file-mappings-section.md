---
title: Seção MapiSvc. inf [mapeamentos do arquivo de ajuda]
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
# <a name="mapisvcinf-help-file-mappings-section"></a>Seção MapiSvc. inf [mapeamentos do arquivo de ajuda]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[help file Mappings]** contém entradas que cada mapa de um serviço de mensagens para o arquivo que fornece ajuda para erros gerados pelo serviço. As entradas nesta seção usam o seguinte formato: 
  
 **[Mapeamentos do arquivo de ajuda]** _nome do serviço de mensagens_  =   _Nome do arquivo de ajuda_
  
O nome do serviço de mensagens é o nome do serviço de mensagens instalado; o nome do arquivo de ajuda é o nome do arquivo onde residem as informações de erro. O exemplo a seguir mostra uma seção típica **[mapeamentos de arquivos de ajuda]** que contém entradas para três serviços: MAPI, o serviço MsgService e o serviço MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


