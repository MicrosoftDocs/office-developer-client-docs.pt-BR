---
title: Seção MapiSvc.inf [Mapeamentos do Arquivo de ajuda]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 776f797d0c96d9173e114fd499d6cca0494a0a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768026"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Seção MapiSvc.inf [Mapeamentos do Arquivo de ajuda]

  
  
**Aplica-se a**: Outlook 
  
A seção **[Help File Mappings]** contém entradas que cada um mapa de um serviço de mensagem para o arquivo que fornece ajuda para erros gerados pelo serviço. Entradas nesta seção usam o seguinte formato: 
  
 **[Mapeamentos do arquivo de ajuda]** _nome do serviço de mensagem_  =   _Nome do arquivo de ajuda_
  
O nome do serviço de mensagem é o nome do serviço de mensagem instalado; o nome do arquivo de Ajuda é o nome do arquivo em que residem as informações de erro. O exemplo a seguir mostra uma seção **[Help File Mappings]** típica que contém as entradas para os três serviços: MAPI, o serviço de MsgService e o serviço MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


