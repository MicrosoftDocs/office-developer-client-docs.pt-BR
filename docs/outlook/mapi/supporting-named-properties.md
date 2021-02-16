---
title: Suporte a propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434323"
---
# <a name="supporting-named-properties"></a>Suporte a propriedades nomeadas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. O suporte para propriedades nomeadas é necessário para: 
  
- Provedores de agendas que permitem que entradas de outros provedores sejam copiadas para seus contêineres.
    
- Provedores de armazenamento de mensagens que podem ser usados para criar tipos de mensagens arbitrários.
    
O suporte a propriedades nomeadas é opcional para todos os outros provedores de serviços. Os provedores de serviços que suportam propriedades nomeadas devem implementar o mapeamento de nome para identificador nos métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Os clientes chamam **GetNamesFromIDs** para recuperar os nomes correspondentes de um ou mais identificadores de propriedade no intervalo 0x8000 e **GetIDsFromNames** para criar ou recuperar os identificadores de um ou mais nomes. 
  
Os provedores de serviços que não suportam propriedades nomeadas devem:
  
- Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array. 
    
- Retorne MAPI_E_NO_SUPPORT dos métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
    

