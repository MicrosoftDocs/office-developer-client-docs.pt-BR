---
title: Escrevendo código do servidor de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a93e53261d56e452f38e38da427585cecccba405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325786"
---
# <a name="writing-form-server-code"></a>Escrevendo código do servidor de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode pensar em um servidor de formulário como o seguinte: 
  
- Um programa Win32 que exibe uma interface e lida com mensagens do Windows por meio dos mecanismos de mecanismo padrão de mecanismo de mensagem do Windows.
    
- Um objeto que registra sua fábrica de classe com OLE e é ativado por métodos de automação OLE.
    
- Um objeto MAPI que segue as regras MAPI para interações com outros componentes MAPI.
    
 Seu código precisa lidar com todos esses três requisitos amplos simultaneamente. 
  
Consulte a seção COM e ActiveX Object Services no SDK do Windows para obter detalhes sobre como registrar a fábrica de classe do servidor de formulário. Manipular mensagens do Windows e exibir uma interface são técnicas de programação padrão do Windows que não têm requisitos especiais em relação a formulários MAPI. Novamente, o SDK do Windows tem detalhes sobre a programação do Windows. Este documento contém o que você precisa saber para implementar as interfaces de formulário MAPI necessárias e opcionais para que elas sigam as regras MAPI para interações com outros componentes MAPI — principalmente o gerenciador de formulário MAPI e aplicativos cliente de mensagens.
  
Todas as interfaces que você pode usar ao implementar servidores de formulário são derivadas direta ou indiretamente da classe base [OLE IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx). Isso significa que todas as implementações dessas interfaces precisarão ter os métodos **QueryInterface,** **AddRef** e **Release.** Você pode economizar muito trabalho se usar várias heranças para implementar todas as interfaces necessárias em uma nova classe, para que todas as interfaces usadas possam compartilhar uma única implementação dos métodos **IUnknown** necessários. Para obter mais informações, consulte os métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)e [IUnknown::Release.](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) Não há considerações especiais em relação aos servidores de formulário MAPI para esses métodos. 
  
Embora nem todas as interfaces de formulário MAPI sejam obrigatórias para todos os servidores de formulário, os métodos em qualquer interface determinada são obrigatórios. Ou seja, se você optar por implementar uma interface específica, deverá implementar todos os métodos na interface. Isso é diferente da situação com alguns outros componentes MAPI, como os transporte de mensagens. Felizmente, os métodos nas interfaces de formulário MAPI são relativamente simples, portanto, implementar todos eles não sobrecarrega muito os desenvolvedores.
  
As interfaces de formulário MAPI são independentes do tipo de ferramenta de desenvolvimento usada para criar um servidor de formulário. Isso permite que formulários sejam criados usando ferramentas de desenvolvimento diferentes. O único requisito é que todos os servidores de formulário devem suportar as interfaces de formulário MAPI necessárias.
  
Nem todas as interfaces MAPI relacionadas a formulários são exigidas por todos os servidores de formulários. As interfaces opcionais permitem que você implemente algumas funções de formulário avançadas que não são necessárias para a maioria dos servidores de formulário. A tabela a seguir lista as interfaces, para que elas são e se você deve implementá-las.
  
|**Interface**|**Descrição**|**Status**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |A interface principal que os clientes usam para carregar servidores de formulário, executar verbos de formulário e desligar servidores de formulário. Essa também é a interface derivada do OLE **IUnknown** que é usada para informar outros componentes OLE sobre quais interfaces um objeto de formulário implementa.  <br/> |Obrigatório  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Usado ao carregar mensagens e salvar mensagens de objetos de formulário.  <br/> |Obrigatório  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Usado por objetos de formulário para controlar o status do cliente de mensagens e para descobrir se o objeto de formulário é capaz de exibir a mensagem seguinte ou anterior em uma pasta.  <br/> |Opcional  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |A interface de fábrica de classe OLE usada por objetos de formulário para conformidade com o mecanismo de fábrica de classe OLE.  <br/> |Obrigatório  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Usado se seu servidor de formulário oferece suporte a mais de um tipo de formulário. Nesse caso, a interface **IMAPIFormFactory** permite que aplicativos cliente acessem as várias interfaces **IClassFactory** (uma por tipo de formulário compatível com seu servidor de formulário) que seu servidor de formulário também deve implementar.  <br/> |Opcional  <br/> |
   
## <a name="see-also"></a>Confira também



[Desenvolvendo servidores de formulário MAPI](developing-mapi-form-servers.md)

