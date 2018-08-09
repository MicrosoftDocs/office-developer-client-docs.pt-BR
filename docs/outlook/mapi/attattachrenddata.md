---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d8c6699ac1bc5687b1c885d156535e5b54b93140
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766199"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Aplica-se a**: Outlook 
  
O atributo **attAttachRenddata** é codificado como uma estrutura **RENDDATA** que descreve como e onde o anexo é processado no texto da mensagem. A estrutura **RENDDATA** é simplesmente codificada no stream TNEF como bytes **sizeof(RENDDATA)** começando com o primeiro membro da estrutura **RENDDATA** . Se o valor do membro de **dwFlags** da estrutura **RENDDATA** é definido como **MAC_BINARY**, em seguida, os dados do anexo a seguir são armazenados no formato MacBinary; Caso contrário, os dados do anexo são codificados como de costume.
  

