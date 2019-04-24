---
title: Enviando mensagens usando o processamento de anexos personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339694"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Enviando mensagens usando o processamento de anexos personalizado TNEF

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para personalizar o processamento de anexos ao enviar uma mensagem:
  
1. Obter um objeto TNEF passando uma interface de **IStream** e uma mensagem para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Obtenha uma lista de todas as propriedades definidas para a mensagem chamando o método [IMAPIProp::](imapiprop-getproplist.md) getproplist. 
    
3. Use os métodos [IMAPIProp](imapipropiunknown.md) para excluir todas as propriedades compatíveis com o sistema de mensagens. Em um momento apropriado, grave essas propriedades no sistema de mensagens no formato exigido pelo sistema de mensagens. 
    
4. Chame o método [ITnef::](itnef-addprops.md) addprops para adicionar somente as propriedades da mensagem, ou seja, nenhuma das propriedades nos anexos, definindo o sinalizador TNEF_PROP_MESSAGE_ONLY. 
    
5. Chamar [ITnef::](itnef-addprops.md) addprops com estes itens: o sinalizador TNEF_PROP_EXCLUDE, uma matriz de marca de propriedade que contém o **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) e um identificador de anexo que especifica o anexo a ser processado.
    
6. Use o método [ITnef::](itnef-setprops.md) SetProps para adicionar a marca de propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) com uma cadeia de caracteres exclusiva que identifica o anexo para o sistema de mensagens se o anexo tiver um nome de arquivo que o o sistema de mensagens não tem suporte. Por exemplo, vários anexos com o mesmo nome de arquivo original ou um nome de arquivo que não é um nome de arquivo válido para o sistema de mensagens. Essa cadeia de caracteres será usada com um número de chave ao gravar as marcas de anexo no texto da mensagem marcada para associar um anexo a seus dados. Para obter mais informações, consulte o [texto da mensagem com tag TNEF](tnef-tagged-message-text.md).
    
7. Repita as **** chamadas addprops e SetProps para cada anexo. **** 
    
8. Chame o método [ITnef:: Finish](itnef-finish.md) para codificar a mensagem no fluxo TNEF após todas as propriedades solicitadas serem adicionadas. 
    
9. Obtenha o texto da mensagem marcada chamando o método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) . Esse texto marcado é lido usando métodos da interface **IStream** , codificados usando o modelo de anexo do sistema de mensagens e gravados no sistema de mensagens. 
    
10. Chame o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar o objeto [ITnef](itnefiunknown.md) . 
    
11. Grave os anexos restantes no sistema de mensagens por meio do modelo de anexo do sistema de mensagens.
    
Seu provedor de transporte deve usar o procedimento descrito anteriormente para processar anexos. Se isso não for possível, o provedor de transporte deverá usar as etapas a seguir para o processamento de anexos personalizado:
  
1. O provedor de transporte garante que as propriedades **PR_ATTACH_TRANSPORT_NAME** de todos os anexos contenham valores exclusivos que são identificadores de anexos válidos para o sistema de mensagens. 
    
2. O provedor de transporte usa uma única chamada para **ITnef::** addprops para cada anexo, passando o sinalizador TNEF_PROP_CONTAINED. 
    

