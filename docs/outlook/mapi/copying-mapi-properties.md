---
title: Copiar propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415044"
---
# <a name="copying-mapi-properties"></a>Copiar propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes e provedores de serviços podem copiar uma ou mais propriedades de um objeto com os seguintes métodos e funções de API do **IMAPIProp** : 
  
- O método [IMAPIProp:: CopyTo](imapiprop-copyto.md) copia Todas as propriedades de um objeto para outro objeto, opcionalmente excluindo as propriedades selecionadas. **CopyTo** é usado para copiar ou mover qualquer tipo de objeto. 
    
- O método [IMAPIProp:: CopyProps](imapiprop-copyprops.md) copia as propriedades selecionadas de um objeto. **CopyProps** é usado principalmente com mensagens. Quando um cliente cria uma cópia encaminhada de uma mensagem ou uma resposta, **CopyProps** as alças de cópia das propriedades apropriadas da mensagem original. 
    
- A função [PropCopyMore](propcopymore.md) copia um valor de propriedade única de um local para outro. Use **PropCopyMore** com cuidado. É possível: ao copiar um valor por vez, para alocar vários blocos pequenos de memória e fazer com que a memória seja fragmentada. 
    
- A função [ScCopyProps](sccopyprops.md) copia valores de propriedade em massa. **ScCopyProps** pode copiar valores de propriedade que foram criados a partir de blocos de memória não conjuntos. Ele retorna uma nova matriz de propriedade. 
    
- Se a matriz de propriedades retornada por **ScCopyProps** for armazenada no disco, use a função [ScRelocProps](screlocprops.md) para ajustar os ponteiros. **ScRelocProps** deve ser chamado duas vezes; uma vez para ajustar os endereços antes de gravar a operação de dados e, em seguida, novamente durante a operação de leitura. A função **ScRelocProps** pressupõe que a matriz de valor da propriedade foi originalmente alocada em uma única alocação. 
    
As funções da API descritas na lista anterior copiam Propriedades na memória, em vez de um objeto para outro objeto. Essas funções têm suporte no momento, mas podem não ser suportadas em uma versão futura.
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

