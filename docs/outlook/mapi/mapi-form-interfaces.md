---
title: Interfaces de formulário MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412342"
---
# <a name="mapi-form-interfaces"></a>Interfaces de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define as seguintes interfaces relacionadas aos formulários.
  
|**Nome da interface**|**Descrição**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Manipula objetos Form e manipula comandos do objeto Form.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Determina se o objeto Form pode manipular a mensagem seguinte e altera o estado seguinte ou anterior do objeto Form.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Oferece suporte à instalação, à desinstalação e à resolução de servidores de formulário em um contêiner de formulário específico.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Dá suporte ao uso de servidores de formulário de tempo de execução configuráveis.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Permite que os aplicativos cliente trabalhem com propriedades específicas de uma classe de mensagem.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Permite que os aplicativos cliente obtenham informações sobre os servidores de formulário, ativa os servidores de formulário e instala os servidores de formulário no sistema de mensagens.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Usado para manipular mensagens associadas a objetos de formulário.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Notifica os aplicativos clientes de que um evento ocorreu no objeto Form.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Usado para responder a comandos Next, Previous e Delete no objeto Form.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Usado para salvar, inicializar e carregar objetos de formulário de e para o armazenamento de mensagens.  <br/> |
   
Para obter mais informações sobre os métodos das interfaces de formulário MAPI, consulte a documentação dessas interfaces. Você não precisa implementar todas as interfaces de formulário MAPI para criar um formulário personalizado. Um formulário em si requer apenas que você implemente as interfaces **IPersistMessage**, **IMAPIForm**e **IMAPIFormAdviseSink** . Além disso, também é uma boa ideia implementar o **IMAPIFormFactory** e o **IMAPIFormInfo**. O **IMAPIFormFactory** é útil para conformidade com OLE e o **IMAPIFormInfo** permite que aplicativos clientes bem escritos usem melhor o uso de seus formulários. 
  
> [!NOTE]
> Estritamente falando, **IMAPIFormAdviseSink** é uma interface opcional. No enTanto, é altamente recomendável que você o implemente nos seus servidores de formulário. Essa interface é crítica para uma interação eficiente entre clientes de mensagens e servidores de formulário, especialmente quando várias mensagens da classe de mensagens do seu servidor de formulário são lidas com o. 
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

