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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382523"
---
# <a name="encoding-a-message-with-tnef"></a>Codificar uma mensagem com TNEF

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando uma mensagem é enviada, o provedor de transporte pode criar um arquivo que é usado para conter a mensagem durante a transmissão. Em seguida, uma interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) é disposta ao redor do arquivo. O provedor de transporte, em seguida, usa os métodos [ITnef](itnefiunknown.md) para gravar as propriedades da mensagem fluxo em um formato marcado que permite que as propriedades a ser facilmente decodificado pelos provedores de recebimento de transporte. 
  
**Para representar uma mensagem inteira em um único arquivo**
  
1. Obter um objeto TNEF ao passar um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e uma mensagem para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Obtenha uma lista de todas as propriedades definidas para a mensagem chamando o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
3. Use métodos [IMAPIProp](imapipropiunknown.md) para excluir todas as propriedades suportadas pelo sistema de mensagens. Em um horário adequado, grave essas propriedades para o sistema de mensagens no formato exigido pelo sistema de mensagens. 
    
4. Chame [ITnef::AddProps](itnef-addprops.md) para codificar as propriedades restantes, incluindo todos os anexos. 
    
5. Chame o método [ITnef::Finish](itnef-finish.md) para codificar a mensagem no fluxo TNEF depois que todas as propriedades solicitadas são adicionadas. 
    
6. Chame o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para obter o texto da mensagem marcados. Esse texto marcado é gravado em um sistema de mensagens usando os métodos da interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) do OLE. 
    
7. Chame o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) para liberar o objeto **ITnef** . 
    
**Para processar uma mensagem de entrada TNEF**
  
1. Obter um objeto de mensagem MAPI do spooler MAPI e propriedades de cabeçalho da mensagem de gravação para a nova mensagem MAPI.
    
2. Criar e inicializar um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para conter os dados TNEF da mensagem de entrada. 
    
3. Passe a mensagem MAPI e o objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
4. Decodificar as informações nos dados TNEF chamando o método [ITnef::ExtractProps](itnef-extractprops.md) . 
    
   > [!NOTE]
   > Nada decodificada por **ExtractProps** substituirá propriedades decodificadas do envelope da mensagem de entrada. Ou seja, propriedades extraídas de TNEF substituirá as propriedades existentes em uma mensagem. 
  
5. Processar o texto da mensagem marcados chamando [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) e analisar o texto para recuperar as posições de anexo. 
    
6. Salve a mensagem chamando [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
7. Libere o objeto TNEF chamando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . 
    

