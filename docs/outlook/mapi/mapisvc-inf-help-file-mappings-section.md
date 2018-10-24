---
title: Seção MapiSvc.inf [Mapeamentos do Arquivo de ajuda]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 91c69489e1a72c5cd702a3c4d0392220a89c38fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580380"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Seção MapiSvc.inf [Mapeamentos do Arquivo de ajuda]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[Help File Mappings]** contém entradas que cada um mapa de um serviço de mensagem para o arquivo que fornece ajuda para erros gerados pelo serviço. Entradas nesta seção usam o seguinte formato: 
  
 **[Mapeamentos do arquivo de ajuda]** _nome do serviço de mensagem_  =   _Nome do arquivo de ajuda_
  
O nome do serviço de mensagem é o nome do serviço de mensagem instalado; o nome do arquivo de Ajuda é o nome do arquivo em que residem as informações de erro. O exemplo a seguir mostra uma seção **[Help File Mappings]** típica que contém as entradas para os três serviços: MAPI, o serviço de MsgService e o serviço MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


