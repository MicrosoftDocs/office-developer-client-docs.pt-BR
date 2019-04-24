---
title: Codificar uma mensagem com TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336698"
---
# <a name="encoding-a-message-with-tnef"></a>Codificar uma mensagem com TNEF

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando uma mensagem é enviada, o provedor de transporte pode criar um arquivo que é usado para conter a mensagem durante a transmissão. Em seguida, uma interface de [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) é colocada em torno do arquivo. O provedor de transporte usa métodos [ITnef](itnefiunknown.md) para gravar as propriedades de mensagem no Stream em um formato marcado que permite que as propriedades sejam facilmente decodificadas pelos provedores de transporte de recebimento. 
  
**Para representar uma mensagem inteira em um único arquivo**
  
1. Obter um objeto TNEF passando um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e uma mensagem para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Obtenha uma lista de todas as propriedades definidas para a mensagem chamando o método [IMAPIProp::](imapiprop-getproplist.md) getproplist. 
    
3. Use os métodos [IMAPIProp](imapipropiunknown.md) para excluir todas as propriedades compatíveis com o sistema de mensagens. Em um momento apropriado, grave essas propriedades no sistema de mensagens no formato exigido pelo sistema de mensagens. 
    
4. Chamar [ITnef::](itnef-addprops.md) addprops para codificar as propriedades restantes, incluindo todos os anexos. 
    
5. Chame o método [ITnef:: Finish](itnef-finish.md) para codificar a mensagem no fluxo TNEF após todas as propriedades solicitadas serem adicionadas. 
    
6. Chame o método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) para obter o texto da mensagem marcada. Este texto marcado é gravado no sistema de mensagens usando métodos da interface do OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
    
7. Chame o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) para liberar o objeto **ITnef** . 
    
**Para processar uma mensagem TNEF de entrada**
  
1. Obtenha um objeto Message MAPI do spooler MAPI e grave as propriedades do cabeçalho da mensagem na nova mensagem MAPI.
    
2. Criar e inicializar um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para conter os dados TNEF da mensagem de entrada. 
    
3. Passe a mensagem MAPI e o objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
4. DeCodifique as informações nos dados TNEF chamando o método [ITnef:: ExtractProps](itnef-extractprops.md) . 
    
   > [!NOTE]
   > Qualquer coisa decodificada pelo **ExtractProps** substituirá as propriedades decodificadas do envelope da mensagem de entrada. Ou seja, as propriedades TNEF extraídas substituirão as propriedades existentes em uma mensagem. 
  
5. Processe o texto da mensagem marcada chamando [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) e analise o texto para recuperar as posições dos anexos. 
    
6. Salve a mensagem chamando [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
7. Libere o objeto TNEF chamando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . 
    

