---
title: Manipular erros de propriedade nomeados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 98b6adbc3a31994768a78b389e16eb3a6ece34bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299367"
---
# <a name="handling-named-property-errors"></a>Manipular erros de propriedade nomeados
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop. 
  
Quando uma chamada como resultado sucesso parcial, como quando a solicita��o � para nomes que mapeiam aos identificadores espec�ficos e um ou mais nomes n�o for encontrado, **GetNamesFromIDs** retorna MAPI_W_ERRORS_RETURNED e coloca PT_ERROR no tipo de propriedade para a propriedade ausente na matriz de marca de propriedade. 
  
Em alguns casos, um cliente faz uma chamada para **GetNamesFromIDs** que resulte em nenhuma propriedades sendo retornadas, como quando n�o h� nenhuma propriedade em um conjunto de propriedades especificado, ou quando todas as propriedades nomeadas s�o de um tipo exclu�do com os sinalizadores. Os clientes podem esperar provedores de servi�os: 
  
- Retorne S_OK.
    
- Defina o conte�do do ponteiro de matriz a propriedade tag para uma matriz de marca de propriedade alocadas recentemente com sua lista de membros **cValues** definida como zero. 
    
- Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL. 
    
- Defina o conte�do da contagem de estruturas de **MAPINAMEID** como zero. 
    
## <a name="see-also"></a>Confira também

- [MAPI denominada propriedades](mapi-named-properties.md)

