---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569446"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attAttachRenddata** é codificado como uma estrutura **RENDDATA** que descreve como e onde o anexo é processado no texto da mensagem. A estrutura **RENDDATA** é simplesmente codificada no stream TNEF como bytes **sizeof(RENDDATA)** começando com o primeiro membro da estrutura **RENDDATA** . Se o valor do membro de **dwFlags** da estrutura **RENDDATA** é definido como **MAC_BINARY**, em seguida, os dados do anexo a seguir são armazenados no formato MacBinary; Caso contrário, os dados do anexo são codificados como de costume.
  

