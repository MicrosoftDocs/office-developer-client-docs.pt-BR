---
title: Adiar erros MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3d2a46be04f235ba55aa5f2feef222ea7372b211
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569859"
---
# <a name="deferring-mapi-errors"></a>Adiar erros MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns m�todos de interface aceitam o sinalizador MAPI_DEFERRED_ERRORS como um par�metro de entrada. Quando esse sinalizador estiver definido, o m�todo n�o precisa retornar imediatamente com um valor; ele pode permitir que o chamador sabe o resultado da chamada em algum momento posterior.
  
Adiar erros ajuda a provedores de servi�os em sua implementa��o dos m�todos complexas, tornando mais r�pido de processamento. Em vez de muitas solicita��es de manipula��o e retornar um valor para cada um, adiar erros permite que as chamadas para ser inclu�do no provedor de servi�o. Processando v�rias solicita��es de uma s� vez recorta no tr�fego de rede, melhorando o desempenho. Adiar erros � especialmente �til nas chamadas para excluir ou propriedades de c�pia, que podem ser muito demoradas opera��es. 
  
Quando um cliente faz uma chamada sem definindo o sinalizador MAPI_DEFERRED_ERRORS que s� pode ser administrado de uma maneira adiada, provedores de servi�os podem adiar ou erros independentemente ou retornar MAPI_E_TOO_COMPLEX. A maioria dos clientes deve adiar erros como uma estrat�gia prefer�vel para falhando a chamada. 
  
Definindo o MAPI_DEFERRED_ERRORS sinalizador altera o tratamento de implementa��o em que as informa��es retornadas podem ser entregues a qualquer momento, em vez de cada vez planejada de erros de um cliente. � poss�vel que um erro a ser retornado quando for muito tarde fazer nada sobre ele ou depois de dados sobre a solicita��o original n�o est�o mais dispon�veis. Por exemplo, se um cliente chama **IMsgStore::OpenEntry** para abrir uma pasta exclu�da com MAPI_DEFERRED_ERRORS definido, o cliente n�o vai saber do problema at� que for feita uma chamada de **IMAPIProp::GetProps** para recuperar uma das propriedades da pasta. **GetProps** retornar� E_NOT_FOUND. 
  
## <a name="see-also"></a>Ver tamb�m



[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)

