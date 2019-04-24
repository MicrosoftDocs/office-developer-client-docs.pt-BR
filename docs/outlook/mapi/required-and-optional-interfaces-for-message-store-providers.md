---
title: Interfaces obrigatórias e opcionais para provedores de repositórios de mensagens
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 35b1d05d742b0d8defabf84b6dbf7d418ece0bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345707"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces obrigatórias e opcionais para provedores de repositórios de mensagens

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI define um conjunto de interfaces relacionadas a provedores de repositório de mensagens. Por causa da ampla variedade de recursos que um repositório de mensagens pode optar por implementar, algumas dessas interfaces são necessárias e outras não. A tabela a seguir lista as interfaces MAPI relacionadas a provedores de repositórios de mensagens, especifica se as interfaces são obrigatórias ou opcionais e descreve sua finalidade.
  
|**Interface**|**Status**|**Descrição**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Obrigatório  <br/> |Faz logon e logoff em um repositório de mensagens.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Obrigatório  <br/> |Abre pastas ou mensagens, verifica a identidade do repositório de mensagens e manipula notificações.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Obrigatório  <br/> |Abre pastas ou mensagens, localiza pastas especiais e manipula envios de mensagens.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Obrigatório  <br/> |Localiza e manipula mensagens e subpastas.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Obrigatório  <br/> |Manipula anexos e define algumas propriedades de uma mensagem.  <br/> |
|[Método](imapitableiunknown.md) <br/> |Obrigatório  <br/> |Permite que outros objetos apresentem conjuntos de dados para vários componentes MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Obrigatório  <br/> |Permite que os clientes validem o estado de um repositório de mensagens e executem algumas tarefas de configuração.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Opcional  <br/> |Acessa as propriedades do anexo de mensagens se o provedor de repositório suportar anexos de arquivo.  <br/> |
|**IStorage** <br/> |Opcional  <br/> |Gerencia objetos de armazenamento estruturados se o provedor de repositórios oferecer suporte a anexos de objeto OLE.  <br/> |
|**IStream** <br/> |Opcional  <br/> |Habilita objetos Message e Attachment para ler e gravar dados em objetos Stream.  <br/> |
|**IStreamDocfile** <br/> |Opcional  <br/> |Permite que alguns provedores de serviços Abram um objeto de armazenamento, como um arquivo composto no formato de arquivo OLE 2,0.  <br/> |
   
As informações básicas de que você precisa para implementar o **IMAPIFolder**, o **IMessage**, o **IMAPIStatus**e o imapitator estão documentadas nos tópicos de referência para essas interfaces. **** Esta seção contém informações complementares que estão mais diretamente relacionadas aos provedores de repositório de mensagens. O restante das interfaces MAPI deve ser implementado de acordo com as informações nesta seção e nos tópicos de referência apropriados. Consulte a seção de serviços de objeto COM e ActiveX no SDK do Windows para obter mais informações sobre a implementação de **IStorage**, **IStream**e **IStreamDocFile**.
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

