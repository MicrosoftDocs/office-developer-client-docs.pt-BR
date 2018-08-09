---
title: Chamado de tratamento de erros de propriedade
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9ea1c4063c08844052618c50fe53fdc0064787a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766677"
---
# <a name="handling-named-property-errors"></a>Chamado de tratamento de erros de propriedade
  
**Aplica-se a**: Outlook 
  
When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop. 
  
Quando uma chamada como resultado sucesso parcial, como quando a solicita��o � para nomes que mapeiam aos identificadores espec�ficos e um ou mais nomes n�o for encontrado, **GetNamesFromIDs** retorna MAPI_W_ERRORS_RETURNED e coloca PT_ERROR no tipo de propriedade para a propriedade ausente na matriz de marca de propriedade. 
  
Em alguns casos, um cliente faz uma chamada para **GetNamesFromIDs** que resulte em nenhuma propriedades sendo retornadas, como quando n�o h� nenhuma propriedade em um conjunto de propriedades especificado, ou quando todas as propriedades nomeadas s�o de um tipo exclu�do com os sinalizadores. Os clientes podem esperar provedores de servi�os: 
  
- Retorne S_OK.
    
- Defina o conte�do do ponteiro de matriz a propriedade tag para uma matriz de marca de propriedade alocadas recentemente com sua lista de membros **cValues** definida como zero. 
    
- Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL. 
    
- Defina o conte�do da contagem de estruturas de **MAPINAMEID** como zero. 
    
## <a name="see-also"></a>Ver tamb�m

- [MAPI denominada propriedades](mapi-named-properties.md)

