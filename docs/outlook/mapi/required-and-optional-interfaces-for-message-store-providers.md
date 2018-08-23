---
title: Interfaces obrigatórias e opcionais para provedores do repositório de mensagens
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 3305aaadbcf7d53b801ddaf7e31a0d63145fc7ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586960"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces obrigatórias e opcionais para provedores do repositório de mensagens

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define um conjunto de interfaces que se relacionam com provedores de armazenamento de mensagem. Devido a ampla gama de recursos que pode escolher implementar um armazenamento de mensagens, algumas dessas interfaces são necessárias e alguns não são. A tabela a seguir lista as interfaces MAPI que estão relacionadas a provedores de repositório de mensagem, especifica se as interfaces são obrigatórias ou opcionais e descreve suas finalidades.
  
|**Interface**|**Status**|**Descrição**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Obrigatório  <br/> |Logs de logon e logoff um armazenamento de mensagens.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Obrigatório  <br/> |Abre pastas ou mensagens, verifica a identidade do repositório de mensagem e manipula notificações.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Obrigatório  <br/> |Abre pastas ou mensagens, localiza pastas especiais e trata envios de mensagem.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Obrigatório  <br/> |Localiza e manipula mensagens e subpastas.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Obrigatório  <br/> |Manipula anexos e define algumas das propriedades da mensagem.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Obrigatório  <br/> |Permite que os outros objetos apresentar os conjuntos de dados para diversos componentes MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Obrigatório  <br/> |Permite que os clientes para validar o estado de um armazenamento de mensagens e executar algumas tarefas de configuração.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Opcional  <br/> |Acessa as propriedades de anexo da mensagem se o provedor de armazenamento oferece suporte a anexos de arquivo.  <br/> |
|**IStorage** <br/> |Opcional  <br/> |Gerencia objetos de armazenamento estruturado se o provedor de armazenamento oferece suporte a anexos de objeto OLE.  <br/> |
|**IStream** <br/> |Opcional  <br/> |Permite que os objetos de mensagem e o anexo para ler e gravar dados em objetos stream.  <br/> |
|**IStreamDocfile** <br/> |Opcional  <br/> |Permite que alguns provedores de serviços abrir um objeto de armazenamento, como um arquivo composto no formato de arquivo OLE 2.0.  <br/> |
   
Os tópicos de referência para essas interfaces documentadas as informações básicas que você precisa implementar **IMAPIFolder**, **IMessage**, **IMAPIStatus**e **IMAPITable** . Esta seção contém informações complementares que está mais diretamente relacionadas aos provedores de armazenamento de mensagem. O restante das interfaces MAPI deve ser implementado de acordo com as informações nesta seção e nos tópicos de referência apropriado. Consulte a seção Serviços de objetos ActiveX e COM no SDK do Windows para obter mais informações sobre como implementar **IStorage**e **IStream** **IStreamDocFile**.
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor do repositório de mensagens MAPI](developing-a-mapi-message-store-provider.md)

