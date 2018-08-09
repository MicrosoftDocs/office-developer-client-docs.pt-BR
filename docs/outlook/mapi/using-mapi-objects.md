---
title: Como usar objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a355faf85a44f6257b77b7171aa965faabf57fe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770702"
---
# <a name="using-mapi-objects"></a>Como usar objetos MAPI

**Aplica-se a**: Outlook 
  
Clientes e provedores de serviço usam objetos MAPI chamando os métodos em suas implementações de interface. Isso é a única maneira que os objetos MAPI podem ser usados; métodos que são implementados por um objeto fora de uma interface MAPI não são acessíveis publicamente. Como todas as interfaces de um objeto estão relacionadas por meio de herança, o usuário de um objeto pode chamar métodos na interface base ou uma das interfaces herdadas conforme se eles pertencem a mesma interface. 
  
Quando o usuário de um objeto deseja fazer uma chamada para um método e esse objeto implementa várias interfaces relacionadas por meio de herança, o usuário não precisa saber ao qual interface o método pertence. O usuário pode chamar qualquer um dos métodos em qualquer uma das interfaces com um único ponteiro para o objeto. Por exemplo, a ilustração a seguir mostra como um aplicativo cliente usa um objeto folder. Objetos de pasta implementar o [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface, que herda de [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indiretamente até [IMAPIProp: IUnknown](imapipropiunknown.md) e [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). Um cliente pode chamar um dos métodos **IMAPIProp** , como [IMAPIProp::GetProps](imapiprop-getprops.md)e uma do [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) métodos, como [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), da mesma maneira com o mesmo ponteiro de objeto. Um cliente não está ciente ou afetados pelo fato de que essas chamadas pertencem a interfaces diferentes.
  
**Client use of a folder object**
  
![Usar o cliente de um objeto folder] (media/amapi_40.gif "Usar o cliente de um objeto folder")
  
Essas chamadas traduzem em código de forma diferente, dependendo se o cliente fazendo as chamadas é gravado em C ou C++. Antes de qualquer chamada para um método pode ser feita, um ponteiro para a implementação de interface deve ser recuperado. Ponteiros de interface podem ser obtidos das seguintes maneiras:
  
- Chamar um método em um objeto diferente.
    
- Chamar uma função API.
    
- Chamar o método de [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) no objeto de destino. 
    
MAPI fornece vários métodos e funções da API que retornam ponteiros para implementações de interface. Por exemplo, os clientes podem chamar o método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para recuperar um ponteiro para um objeto table que fornece acesso às informações do provedor de repositório de mensagens por meio do [IMAPITable: IUnknown](imapitableiunknown.md) interface. Provedores de serviços podem chamar a função de API [CreateTable](createtable.md) para recuperar um ponteiro para um objeto de dados de tabela. Quando não há nenhuma função ou o método disponível e clientes ou provedores de serviço já tem um ponteiro para um objeto, eles podem chamar o método do objeto **QueryInterface** para recuperar um ponteiro para outro de implementações de interface do objeto. 
  
## <a name="see-also"></a>Confira também

- [Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

