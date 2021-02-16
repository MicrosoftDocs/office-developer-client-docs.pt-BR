---
title: Objetos de formulário personalizados MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318240"
---
# <a name="mapi-custom-form-objects"></a>Objetos de formulário personalizados MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os objetos para formulários personalizados são implementados por três componentes diferentes:
  
- Um servidor de formulário.
    
- Um provedor de biblioteca de formulário.
    
- Um visualizador de formulário.
    
Um servidor de formulário é semelhante em funcionalidade a um aplicativo de objeto de documento composto OLE. É um componente executável que implementa o formulário; ele controla sua exibição e as operações que um usuário pode executar. MAPI starts a form server upon request when a user wants to view a message together with a message class that is displayed by using a form supported by the form server. Os servidores de formulário implementam três objetos: um objeto de fábrica de formulário que se parece com o fábrica de classe OLE padrão, um sink de consultoria de formulário para manipular eventos específicos do formulário e o próprio formulário. 
  
Um provedor de biblioteca de formulário fornece acesso para clientes ao conjunto de propriedades de um formulário, ao seu contêiner e ao objeto que vincula mensagens de uma classe específica ao servidor que pode abrir o formulário para essa classe. Os provedores de biblioteca de formulário implementam três objetos: um objeto de informações de formulário, um contêiner de formulário e um gerenciador de formulário para vincular uma mensagem ao servidor de formulário apropriado com base na classe da mensagem.
  
Um visualizador de formulários é um componente incluído em clientes que suportam a exibição de formulários personalizados em seus visualizadores de pasta. Visualizadores de formulário não são componentes MAPI independentes, assim como provedores de biblioteca de formulário e servidores de formulário. Visualizadores de formulário iniciam servidores de formulário e fornecem contexto para eles. Visualizadores de formulário implementam três objetos: um site de mensagens, um contexto de exibição e um evento de aconselhá-los para manipular eventos específicos de exibição.
  
A tabela a seguir descreve todos os objetos de formulário personalizados. 
  
|**Objeto Form**|**Descrição**|
|:-----|:-----|
|Formulário  <br/> |Controla a exibição e a operação de um formulário personalizado para exibir mensagens de uma classe específica.  <br/> |
|Pia de aconselhmento de formulário  <br/> |Lida com notificações do visualizador de formulário.  <br/> |
|Fábrica de formulário  <br/> |Cria uma instância de um formulário e permite que seu servidor permaneça na memória.  <br/> |
|Contêiner de formulário  <br/> |Contém informações de formulário.  <br/> |
|Informações do formulário  <br/> |Contém mensagens e outros contêineres de mensagens.  <br/> |
|Gerente de formulário  <br/> |Fornece acesso a uma exibição integrada de informações de formulário personalizado relacionadas a todos os formulários instalados. Também corresponde às classes de mensagens com identificadores de classe de formulário correspondentes.  <br/> |
|Site de mensagens  <br/> |Manipula a manipulação de objetos de formulário de dentro do cliente e fornece acesso a um objeto gerenciador de formulário.  <br/> |
|Exibir contexto  <br/> |Oferece suporte a comandos de formulário para ativar mensagens próximas e anteriores e para salvar ou imprimir.  <br/> |
|View advise sink  <br/> |Lida com notificações do servidor de formulário.  <br/> |
   
A ilustração a seguir mostra a relação entre componentes de formulário personalizados, os objetos e interfaces que eles implementam e os componentes que são usuários dos objetos. Observe que, ao contrário da maioria dos outros objetos MAPI, o objeto de formulário implementa duas interfaces que não estão relacionadas por herança direta. Quando um objeto expõe várias interfaces independentes, um usuário do objeto que tem um ponteiro para uma das interfaces pode recuperar um ponteiro para qualquer uma das outras interfaces. Essa capacidade de navegar entre implementações de interface de um objeto é um recurso do [método IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) 
  
**Custom form components**
  
![Componentes de formulário personalizados](media/amapi_67.gif "Componentes de formulário personalizados")
  
## <a name="see-also"></a>Confira também

- [Visão geral de objetos e interface MAPI](mapi-object-and-interface-overview.md)

