---
title: Copiando propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2f9ee7221f523d7c92d91746f5cd719fad821a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766334"
---
# <a name="copying-mapi-properties"></a>Copiando propriedades MAPI

  
  
**Aplica-se a**: Outlook 
  
Clientes e provedores de serviços podem copiar uma ou mais das propriedades de um objeto com os seguintes métodos **IMAPIProp** e funções da API: 
  
- O método [IMAPIProp::CopyTo](imapiprop-copyto.md) copia todas as propriedades de um objeto para outro objeto, opcionalmente, excluindo propriedades selecionadas. **CopyTo** é usado para copiar ou mover qualquer tipo de objeto. 
    
- O método [IMAPIProp::CopyProps](imapiprop-copyprops.md) copia propriedades selecionadas de um objeto. **CopyProps** é usado principalmente com mensagens. Quando um cliente cria uma cópia encaminhada de uma mensagem ou uma resposta, alças **CopyProps** copiando as propriedades adequadas a partir da mensagem original. 
    
- A função [PropCopyMore](propcopymore.md) copia um valor de propriedade exclusivo de um local para outro. Use **PropCopyMore** com cautela. É possível — ao copiar um valor ao mesmo tempo — alocar muitos pequenos blocos de memória e fazer com que a memória para fragmentar. 
    
- A função [ScCopyProps](sccopyprops.md) copia os valores de propriedade em massa. **ScCopyProps** pode copiar os valores de propriedade que foram desenvolvidos de blocos não contíguos de memória. Ele retorna uma nova matriz de propriedade. 
    
- Se a matriz de propriedade retornada por **ScCopyProps** deve ser armazenado em disco, use a função [ScRelocProps](screlocprops.md) para ajustar os ponteiros. **ScRelocProps** deve ser chamado duas vezes; uma vez para ajustar os endereços antes de gravar a operação de dados e, em seguida, novamente durante a operação de leitura. A função **ScRelocProps** pressupõe que a matriz de valores de propriedade foi originalmente alocado em uma única alocação. 
    
As funções da API descritas as propriedades de cópia lista anterior na memória, em vez de um objeto para outro objeto. Essas funções são suportadas atualmente, mas não podem ser suportadas em uma versão futura.
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

