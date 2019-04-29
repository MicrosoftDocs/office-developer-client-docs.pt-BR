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
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427133"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attAttachRenddata** é codificado como uma estrutura **RENDDATA** que descreve como e onde o anexo é renderizado no texto da mensagem. A estrutura **RENDDATA** é simplesmente codificada no fluxo TNEF como **sizeof (RENDDATA)** bytes, começando com o primeiro membro da estrutura **RENDDATA** . Se o valor do membro **dwFlags** da estrutura **RENDDATA** for definido como **MAC_BINARY**, os dados do seguinte anexo serão armazenados no formato MacBinary; caso contrário, os dados de anexo serão codificados como de costume.
  

