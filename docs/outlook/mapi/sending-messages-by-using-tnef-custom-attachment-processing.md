---
title: Enviar mensagens usando o processamento de anexos personalizado com TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388564"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Enviar mensagens usando o processamento de anexos personalizado com TNEF

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para personalizar o processamento de anexo ao enviar uma mensagem:
  
1. Obter um objeto TNEF passando uma interface **IStream** e uma mensagem para a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Obtenha uma lista de todas as propriedades definidas para a mensagem chamando o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
3. Use métodos [IMAPIProp](imapipropiunknown.md) para excluir todas as propriedades suportadas pelo sistema de mensagens. Em um horário adequado grave essas propriedades para o sistema de mensagens no formato exigido pelo sistema de mensagens. 
    
4. Chame o método [ITnef::AddProps](itnef-addprops.md) para adicionar apenas as propriedades da mensagem — ou seja, nenhuma das propriedades nos anexos —, definindo o sinalizador TNEF_PROP_MESSAGE_ONLY. 
    
5. Chamar [ITnef::AddProps](itnef-addprops.md) com estes itens: o sinalizador TNEF_PROP_EXCLUDE, uma matriz de marca de propriedade que contém o **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) propriedade e um identificador de anexo que especifica o anexo a ser processado.
    
6. Use o método [ITnef::SetProps](itnef-setprops.md) para adicionar a marca de propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) com uma cadeia de caracteres exclusiva que identifica o anexo a sistema de mensagens, se o anexo tiver um nome de arquivo que o não oferece suporte ao sistema de mensagens. Por exemplo, vários anexos com o mesmo nome de arquivo original ou um nome de arquivo que não é um nome de arquivo válido para o sistema de mensagens. Esta cadeia de caracteres será ser usada com um número de chave ao escrever as marcas de anexo no texto da mensagem marcados para associar um anexo com seus dados. Para obter mais informações, consulte, [TNEF-Tagged o texto da mensagem](tnef-tagged-message-text.md).
    
7. Repita as chamadas **AddProps** e **SetProps** para cada anexo. 
    
8. Chame o método [ITnef::Finish](itnef-finish.md) para codificar a mensagem no fluxo TNEF depois que todas as propriedades solicitadas são adicionadas. 
    
9. Obter o texto da mensagem marcados chamando o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) . Esse texto marcado é lido usando os métodos da interface **IStream** , codificados usando o modelo de anexo do sistema de mensagens e gravado em um sistema de mensagens. 
    
10. Chame o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar o objeto [ITnef](itnefiunknown.md) . 
    
11. Escreva os anexos restantes para o sistema de mensagens por meio do modelo de anexo do sistema de mensagens.
    
Seu provedor de transporte deve usar o procedimento descrito anteriormente para o processo de anexos. Se não for possível, o provedor de transporte deve usar as seguintes etapas para processamento de anexo personalizada:
  
1. O provedor de transporte garante que as propriedades **PR_ATTACH_TRANSPORT_NAME** de todos os anexos contenham valores exclusivos que são identificadores de anexo válido para o sistema de mensagens. 
    
2. O provedor de transporte, em seguida, usa uma única chamada de **ITnef::AddProps** para cada anexo, passando o sinalizador TNEF_PROP_CONTAINED. 
    

