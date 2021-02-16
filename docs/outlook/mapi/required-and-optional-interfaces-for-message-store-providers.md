---
title: Interfaces opcionais e necessárias para provedores de armazenamento de mensagens
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 35b1d05d742b0d8defabf84b6dbf7d418ece0bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420917"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces opcionais e necessárias para provedores de armazenamento de mensagens

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI define um conjunto de interfaces relacionadas aos provedores de armazenamento de mensagens. Devido à ampla variedade de recursos que um armazenamento de mensagens pode optar por implementar, algumas dessas interfaces são necessárias e outras não. A tabela a seguir lista as interfaces MAPI relacionadas aos provedores de armazenamento de mensagens, especifica se as interfaces são necessárias ou opcionais e descreve sua finalidade.
  
|**Interface**|**Status**|**Descrição**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Obrigatório  <br/> |Faz e sai de um armazenamento de mensagens.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Obrigatório  <br/> |Abre pastas ou mensagens, verifica a identidade do armazenamento de mensagens e lida com notificações.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Obrigatório  <br/> |Abre pastas ou mensagens, localiza pastas especiais e lida com envios de mensagens.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Obrigatório  <br/> |Localiza e manipula mensagens e subpastas.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Obrigatório  <br/> |Manipula anexos e define algumas das propriedades de uma mensagem.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Obrigatório  <br/> |Permite que outros objetos apresentem coleções de dados para vários componentes MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Obrigatório  <br/> |Permite que os clientes validem o estado de um armazenamento de mensagens e realizem algumas tarefas de configuração.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Opcional  <br/> |Acessará as propriedades do anexo da mensagem se o provedor do armazenamento suportar anexos de arquivo.  <br/> |
|**IStorage** <br/> |Opcional  <br/> |Gerencia objetos de armazenamento estruturados se o provedor de armazenamento oferece suporte a anexos de objeto OLE.  <br/> |
|**IStream** <br/> |Opcional  <br/> |Permite que objetos de mensagem e anexo leiam e escrevam dados em objetos de fluxo.  <br/> |
|**IStreamDocfile** <br/> |Opcional  <br/> |Permite que alguns provedores de serviços abram um objeto de armazenamento, como um arquivo composto no formato de arquivo OLE 2.0.  <br/> |
   
As informações básicas necessárias para implementar **IMAPIFolder**, **IMessage**, **IMAPIStatus** e **IMAPITable** estão documentadas nos tópicos de referência para essas interfaces. Esta seção contém informações suplementares que estão mais diretamente relacionadas aos provedores de armazenamento de mensagens. O restante das interfaces MAPI deve ser implementado de acordo com as informações nesta seção e nos tópicos de referência apropriados. Consulte a seção COM e ActiveX Object Services no SDK do Windows para obter mais informações sobre como implementar **IStorage**, **IStream** e **IStreamDocFile**.
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

