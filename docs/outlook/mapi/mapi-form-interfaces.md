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
ms.openlocfilehash: f37d398167e8210a2fd67ff08e63572eb6c9db9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585721"
---
# <a name="mapi-form-interfaces"></a>Interfaces de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define as seguintes interfaces relacionadas aos formulários.
  
|**Nome da interface**|**Descrição**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Manipula a objetos de formulário e trata comandos de objeto do formulário.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Determina se o objeto de formulário pode manipular a próxima mensagem e altera o estado anterior ou seguinte do objeto form.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Oferece suporte à instalação, desinstalação e resolução de servidores de formulário contra um contêiner de formulário específico.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Suporta o uso de servidores de formulário configurável de tempo de execução.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Permite que aplicativos de cliente trabalhar com propriedades que são específicas para uma classe de mensagem.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Permite que os aplicativos de cliente obter mais informações sobre servidores de formulário, ativa a servidores de formulário e instala os servidores de formulário no sistema de mensagens.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Usado para manipular mensagens associadas com objetos de formulário.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Notifica os aplicativos cliente que ocorreu um evento no objeto form.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Usada para responder aos comandos próximo, anterior e excluir o objeto form.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Usado para salvar, inicializar e carregar os objetos de formulário de e para armazenamento de mensagens.  <br/> |
   
Para obter mais informações sobre os métodos das interfaces do formulário MAPI, consulte a documentação para essas interfaces. Você não precisará implementar todas as interfaces de formulário MAPI para criar um formulário personalizado. Um formulário em si só requer que você implementar a **IPersistMessage**, **IMAPIForm**, e **IMAPIFormAdviseSink** interfaces. Além disso, também é uma boa ideia implementar **IMAPIFormFactory** e **IMAPIFormInfo**. **IMAPIFormFactory** é útil para fins de conformidade de OLE e **IMAPIFormInfo** permite que os aplicativos de cliente bem escrito tornar o melhor uso dos seus formulários. 
  
> [!NOTE]
> Rigor, **IMAPIFormAdviseSink** é uma interface opcional. No entanto, é altamente recomendável que você implemente-la em seus servidores do formulário. Esta interface é fundamental para a interação eficiente entre clientes de mensagens e servidores de formulário, especialmente quando várias mensagens do seu servidor de formulário classe de mensagem estão sendo resolvido com. 
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

