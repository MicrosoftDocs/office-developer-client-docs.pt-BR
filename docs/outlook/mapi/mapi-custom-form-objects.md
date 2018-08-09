---
title: Objetos de formulário personalizado do MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ecb40262959834ec511601ec3176887c919d944f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767838"
---
# <a name="mapi-custom-form-objects"></a>Objetos de formulário personalizado do MAPI
  
**Aplica-se a**: Outlook 
  
Objetos de formulários personalizados são implementados por três componentes diferentes:
  
- Um servidor de formulário.
    
- Um provedor de biblioteca de formulário.
    
- Um visualizador de formulário.
    
Um servidor de formulário é semelhante em funcionalidade a um aplicativo de objeto de documento composto OLE. É um componente do executável que implementa o formulário; Ele controla as operações que um usuário pode realizar e sua exibição. MAPI inicia um servidor de formulário mediante solicitação quando um usuário quiser exibir uma mensagem em conjunto com uma classe de mensagem é exibida, usando um formulário compatíveis com o servidor do formulário. Servidores de formulário implementar três objetos: alocador de classe de um objeto de fábrica de formulário que se parece com o OLE padrão, um formulário de aviso coletor de eventos para lidar com eventos específicos de formulário e o próprio formulário. 
  
Um provedor de biblioteca de formulário fornece acesso para clientes para o conjunto de propriedades de um formulário, ao seu contêiner e ao objeto que vincula as mensagens de uma classe específica ao servidor que pode abrir o formulário para a classe. Provedores de biblioteca de formulário implementar três objetos: um objeto de informações de formulário, um contêiner de formulário e um gerente de formulário para uma mensagem de vinculação para o servidor de formulário apropriada com base na classe da mensagem.
  
Um visualizador de formulário é um componente que está incluído nos clientes que dão suporte à exibição de formulários personalizados em seus visualizadores de pasta. Visualizadores de formulário não são componentes MAPI independentes, assim como provedores de biblioteca de formulário e servidores de formulário. Visualizadores de formulário inicie os servidores de formulário e fornecem um contexto para eles. Visualizadores de formulário implementam três objetos: um site de mensagem, um contexto de modo de exibição e um coletor de advise de manipulação de eventos específicos do modo de exibição.
  
A tabela a seguir descreve todos os objetos de formulário personalizado. 
  
|**Objeto Form**|**Descrição**|
|:-----|:-----|
|Formulário  <br/> |Controla a exibição e a operação de um formulário personalizado para exibir mensagens de uma classe específica.  <br/> |
|Coletor de eventos de aviso de formulário  <br/> |Manipula notificações do Visualizador de formulário.  <br/> |
|Alocador de formulário  <br/> |Cria uma instância de um formulário e permite que o seu servidor permaneça na memória.  <br/> |
|Contêiner de formulário  <br/> |Contém informações do formulário.  <br/> |
|Informações do formulário  <br/> |Contém mensagens e outros contêineres de mensagem.  <br/> |
|Gerenciador de formulário  <br/> |Fornece acesso a um modo de exibição integrado das informações de formulário personalizado que estão relacionadas a todos os formulários instalados. Também faz a correspondência de classes de mensagens com identificadores de classe de formulário correspondente.  <br/> |
|Site de mensagem  <br/> |Manipula a manipulação de objetos de formulário de dentro do cliente e fornece acesso a um objeto do Gerenciador de formulário.  <br/> |
|Contexto de modo de exibição  <br/> |Suporte a comandos para ativar as mensagens anteriores e próximas e para salvar ou imprimir de formulário.  <br/> |
|Coletor de eventos de aviso do modo de exibição  <br/> |Manipula notificações do servidor de formulário.  <br/> |
   
A ilustração a seguir mostra a relação entre os componentes de formulário personalizado, os objetos e interfaces que eles implementam e os componentes que são usuários dos objetos. Observe que, ao contrário da maioria dos outros objetos MAPI, o objeto form implementa duas interfaces que não estão relacionados por herança direta. Quando um objeto expõe várias interfaces independentes, um usuário do objeto que tem um ponteiro para uma das interfaces pode recuperar um ponteiro para qualquer uma das outras interfaces. Essa capacidade para navegar entre implementações de interface de um objeto é um recurso do método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . 
  
**Custom form components**
  
![Componentes de formulário personalizado] (media/amapi_67.gif "Componentes de formulário personalizado")
  
## <a name="see-also"></a>Confira também

- [Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

