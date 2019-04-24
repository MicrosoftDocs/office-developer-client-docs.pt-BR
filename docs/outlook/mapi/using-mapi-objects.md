---
title: Usar objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d732efe5276f4756f43b4aca46e1c33d6f103844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329671"
---
# <a name="using-mapi-objects"></a>Usar objetos MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes e provedores de serviço usam objetos MAPI chamando os métodos em suas implementações de interface. Essa é a única maneira que os objetos MAPI podem ser usados; os métodos que são implementados por um objeto fora de uma interface MAPI não são acessíveis publicamente. Como todas as interfaces de um objeto estão relacionadas por meio da herança, o usuário de um objeto pode chamar métodos na interface base ou em uma das interfaces herdadas, como se elas pertencem à mesma interface. 
  
Quando o usuário de um objeto quiser fazer uma chamada para um método e esse objeto implementar várias interfaces relacionadas através da herança, o usuário não precisará saber qual interface o método pertence. O usuário pode chamar qualquer um dos métodos em qualquer uma das interfaces com um único ponteiro para o objeto. Por exemplo, a ilustração a seguir mostra como um aplicativo cliente usa um objeto Folder. Os objetos Folder implementam a interface [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) , que herda de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indiretamente por meio de [IMAPIProp: IUnknown](imapipropiunknown.md) e [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). Um cliente pode chamar um dos métodos **IMAPIProp** , como [IMAPIProp::](imapiprop-getprops.md)GetProps e um dos métodos [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) , como [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md), da mesma maneira que o mesmo ponteiro de objeto. Um cliente não está ciente ou é afetado pelo fato de que essas chamadas pertencem a interfaces diferentes.
  
**Client use of a folder object**
  
![Uso do cliente de um objeto Folder] (media/amapi_40.gif "Uso do cliente de um objeto Folder")
  
Essas chamadas são traduzidas em código de forma diferente, dependendo se o cliente que está fazendo as chamadas é escrito em C ou C++. Antes que qualquer chamada para um método possa ser feita, um ponteiro para a implementação da interface deve ser recuperado. Os ponteiros de interface podem ser obtidos das seguintes maneiras:
  
- Chamar um método em um objeto diferente.
    
- Chamar uma função de API.
    
- Chamando o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) no objeto de destino. 
    
MAPI fornece vários métodos e funções de API que retornam ponteiros para implementações de interface. Por exemplo, os clientes podem chamar o método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para recuperar um ponteiro para um objeto Table que fornece acesso a informações do provedor de repositórios de mensagens por meio da interface IMAPITable [: IUnknown](imapitableiunknown.md) . Os provedores de serviços podem chamar a [](createtable.md) função CreateTable da API para recuperar um ponteiro para um objeto Table Data. Quando não há função ou método disponível e clientes ou provedores de serviço já têm um ponteiro para um objeto, eles podem chamar o método **QueryInterface** do objeto para recuperar um ponteiro para outra das implementações de interface do objeto. 
  
## <a name="see-also"></a>Confira também

- [Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

