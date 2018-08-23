---
title: Gravar um código de servidor de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 463193b55dab0839c756367db16d02aae5980a77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578119"
---
# <a name="writing-form-server-code"></a>Gravar um código de servidor de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode pensar em um servidor de formulário como o seguinte: 
  
- Um programa Win32 que exibe uma interface e trata as mensagens windows por meio de mecanismos de bomba de mensagem padrão do Windows.
    
- Um objeto que registra o respectivo alocador de classe com OLE e está ativado por meio de métodos de automação OLE.
    
- Um objeto MAPI que segue as regras de MAPI para interações com outros componentes MAPI.
    
 Seu código deve lidar com todos os três esses requisitos amplos simultaneamente. 
  
Consulte a seção Serviços de objetos ActiveX e COM no SDK do Windows para obter detalhes sobre como registrar o alocador de classe do seu servidor de formulário. Manipulação de mensagens do windows e exibindo uma interface são standard técnicas de programação de Windows que não tenham requisitos especiais com relação a formulários MAPI. Novamente, o SDK do Windows mostra detalhes sobre a programação do Windows. Este documento contém o que você precisa saber para implementar as interfaces de formulário MAPI obrigatórios e opcionais de modo que eles seguem as regras MAPI para interações com outros componentes MAPI — principalmente MAPI formar manager e aplicativos cliente de mensagens.
  
Todas as interfaces que podem ser usados quando você implementa servidores de formulário são derivadas — direta ou indiretamente — da OLE [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)de classe de base. Isso significa que todas as suas implementações dessas interfaces precisará ter os métodos de **QueryInterface**, **AddRef**e **Release** . Você pode economizar muito trabalho se você usar vários herança para implementar todas as interfaces necessárias em uma nova classe de sua preferência, para que todas as interfaces que você use podem compartilhar uma única implementação dos métodos **IUnknown** necessários. Para obter mais informações, consulte os métodos [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx), [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)e [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) . Não há nenhuma consideração especial em relação aos servidores de formulário MAPI para esses métodos. 
  
Enquanto não todas as interfaces de formulário MAPI são obrigatórias para todos os servidores de formulário, os métodos em uma determinada interface são obrigatórios. Ou seja, se você optar por implementar uma interface particular, você deve implementar todos os métodos na interface do. Isso é diferente da situação com alguns outros componentes MAPI, como transportes de mensagem. Felizmente, os métodos as interfaces de formulário MAPI são relativamente simples, portanto implementar todos eles não coloca uma grande carga nos desenvolvedores.
  
As interfaces de formulário MAPI são independentes do tipo da ferramenta de desenvolvimento usada para criar um servidor de formulário. Isso permite que os formulários a ser criado usando as ferramentas de desenvolvimento diferentes. O único requisito é que todos os servidores do formulário devem suportar as interfaces de formulário MAPI necessárias.
  
Nem todas as interfaces MAPI que se relacionam com formulários são necessárias por todos os servidores do formulário. As interfaces opcionais permitem que você implemente algumas funções avançadas de formulário que não são necessárias para a maioria dos servidores de formulário. A tabela a seguir lista as interfaces, o que são e se você deve implementá-las.
  
|**Interface**|**Descrição**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |A interface principal que são usadas pelos clientes para carregar os servidores do formulário, execute os verbos de formulário e desligar servidores do formulário. Isso também é a interface derivada do OLE **IUnknown** que é usado para informar aos outros componentes do OLE sobre quais interfaces implementa um objeto form.  <br/> |Obrigatório  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Usado quando o carregamento de mensagens em e poupa mensagens de objetos de formulário.  <br/> |Obrigatório  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Usado pelos objetos de formulário para manter o controle de status do cliente de mensagens e para descobrir se o objeto de formulário é capaz de exibir a mensagem anterior ou seguinte em uma pasta.  <br/> |Opcional  <br/> |
|[IClassFactory](http://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |A interface de fábrica de classe OLE utilizada pelos objetos de formulário para fins de conformidade com o mecanismo de fábrica de classe OLE.  <br/> |Obrigatório  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Usado se o seu servidor de formulário oferece suporte a mais de um tipo de formulário. Nesse caso, a interface de **IMAPIFormFactory** permite que os aplicativos clientes para acessar as várias interfaces **IClassFactory** (um por tipo de formulário que ofereça suporte a seu servidor de formulário) que seu servidor de formulário também deve implementar.  <br/> |Opcional  <br/> |
   
## <a name="see-also"></a>Confira também



[Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

